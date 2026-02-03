# Custom code

If you implemented your own eShop, or we do not provide an integration with your eCommerce platform of choice, this article is for you.

Please keep in mind that this is a simple setup that uses `Materials` and `Variants`. If your project/configurator uses other setups you will need to adapt.



## Vectary setup

### 1.1. Create a folder for the product models

This is an important part of any integration. **Use the id of the folder to fetch and map your models to the products** you have/will setup in the e-shop.

You can see the id when it is selected inside the [Dashboard](https://vectary.com/dashboard), directly in the URL after the string `&folderId=`.



### 1.2. Create the model of your product/s

In this case, we created an abstract design called `Awesomeness`. **The name of your project needs to match the name of your product**.

Here is the model you can clone directly into a new project in your workspace: [https://www.vectary.com/p/5s8oStuOPjH9E2xrRVje3q](https://www.vectary.com/p/5s8oStuOPjH9E2xrRVje3q)\
\
It features a `Variant` with 3 different objects, and each of the variants contains the same 3 materials. **Make sure to link the materials if they are the same between each variant**.

We can expose these through the `Floating UI` by adding a `Materials` and a `Variants` sub-objects.

Please note that the `source` of the MSController is the Object Switcher containing the variants.

&#x20;![](<../../../.gitbook/assets/image (123).png>)         ![](<../../../.gitbook/assets/image (124).png>)



### 1.3. Share your model

Go ahead and [share](../../../documentation/sharing-exporting-embedding/sharing.md)

Please remember that:

* The name of the project matches the name of the product.
* The names of the objects and their materials match the options/variants that are setup for the product in the e-shop.



## Custom site setup

### 2.1. Add the HTML

The first thing needed to connect the model to site are the `UI elements` that allow to configure the product in the eshop.

These tipically are `select` inputs with different `options`, but we are not limited to that, it can be anything, like a bunch of different buttons for each property/variant.

Make sure to have the control over those and keep them structured. Here is an example based on the model created from step `1.2`:

```html
<div class="product_config">
    <div class="property">
        <label>Color</label>
        <select>
            <option value="White" selected="">White</option>
            <option value="Grey">Grey</option>
            <option value="Black">Black</option>
        </select>
    </div>
    <div class="property">
        <label>Composition</label>
        <select>
            <option value="First" selected="">First</option>
            <option value="Second">Second</option>
            <option value="Third">Third</option>
        </select>
    </div>
</div>
```

The rundown:

* The whole configuration of the product is wrapped under the class `product_config`.
* Inside, there is a pattern for each `property` that can be changed in the product:
  * `label` with the name of the property
  * `select` element with all the `options` for that property

We could also create a different structure for any of the properties:

```html
<div class="property">
    <label>Color</label>
    <div class="options">
        <button class="active">White</button>
        <button>Grey</button>
        <button>Black</button>
    </div>
</div>
```

Any structure can be used to fit a specific design, but that will change how the code needs to be written to link the `Variants` and `Materials` of the 3D model, to the Product properties in the UI.



### 2.2. Add the 3D Model and the API script

Once the structure matches the product and the 3d model, we can start linking them. First add the `iframe` with the model and the `API script`:

```html
<iframe 
    id="vectary_embed" 
    src="<https://app.vectary.com/p/{shared_model_id}>" 
    frameborder="0" 
    width="100%" 
    height="100%">
</iframe>

<script type="module">
    import { VctrModelApi } from "<https://app.vectary.com/studio-lite/scripts/api.js>";
    var modelApi = new VctrModelApi("vectary_embed");
    await modelApi.init();
    
    // Your code will go here
</script>
```

Please note:

* You need to replace `{shared_model_id}` with the id of the model you want to load at the start.
* Feel free to change the **iframe id** to something else, but remember to also change it in the initialization of the `VctrModelApi`.



### 2.3. Add the custom code

At a very high level we want to **listen to changes from the 3D model, and apply those into the UI of our eshop**, and/or vice-versa.

We will create a JS class to better handle specific parts of the code with some helper functions:

```javascript
class CustomIntegration {
    #selects; // We use selects in our UI, so this implementation will revolve around them
    constructor() {
        this.#selects = document.querySelectorAll("select");
    }

    async init() {}
    
    // Helper functions
    #stateMatches(inputName, stateName) {}
    #loopConfigs(currentConfigs, newConfigs, key, value, options) {}
    
    // Main functions
    async #listenToChangesFromUI() {}
    async #listenToChangesFromModel(configs) {}
}
```

#### init():

In the init function we are going to setup the listeners for "linking" the changes in the UI to the model, and the changes of the model to the UI.

```javascript
async init() {
    // Listen for changes from the UI
    this.#selects.forEach((select) => {
        select.addEventListener(
            "change",
            this.#listenToChangesFromUI.bind(this)
        );
    });

    // Listen for changes from the Model
    await modelApi.addEventListener(
        "configurator_state_change",
        this.#listenToChangesFromModel.bind(this)
    );
}
```

#### #listenToChangesFromUI()

This takes care of looping through the selects and crating a `configurator state` that we can send back to the model with the usage of the `setConfigurationState` API function.

```javascript
async #listenToChangesFromUI() {
    // We need to construct a config state from all the current selects by
    // checking the current config, and filling in the info we are missing from the selects
    const currentConfigArray =
        await modelApi.getConfigurationState();
    const newConfigArray = [];

    // First round focusing on the ObjectSwitchers,
    // since the following material options need to affect these
    for (const select of this.#selects) {
        this.#loopConfigs(
            currentConfigArray,
            newConfigArray,
            "active_object",
            select.value,
            Array.from(select.options)
        );
    }

    // Second round to check on the MaterialSwitchers
    for (const select of this.#selects) {
        this.#loopConfigs(
            currentConfigArray,
            newConfigArray,
            "active_material",
            select.value,
            Array.from(select.options)
        );
    }

    // Apply the new configs to the model
    if (newConfigArray.length > 0)
        await modelApi.setConfigurationState(newConfigArray);
}
```

#### #listenToChangesFromModel()

This function is what we pass to the callback of the `configurator_state_change` API event, so we can apply changes to the UI on the website when changes are made to the 3D model's `Floating UI`.

```javascript
async #listenToChangesFromModel(configs) {
    // Helper functions
    const isObjectSwitcherState = (config) =>
        "active_object" in config;
    const isMaterialSwitcherState = (config) =>
        "active_material" in config;

    // Run through the configs and store them separately
    const objectSwitchers = new Map();
    const materialSwitchers = [];
    configs.forEach((config) => {
        // Config can be either a Material Switcher or an Object Switcher,
        // and OS are always first
        if (isObjectSwitcherState(config))
            objectSwitchers.set(
                config.active_object_instanceId,
                config
            );
        // Filter all MS that are not from an active variant
        else if (
            isMaterialSwitcherState(config) &&
            objectSwitchers.has(config.object_instanceId)
        )
            materialSwitchers.push(config);
    });

    // Update the selects with the new configs
    this.#selects.forEach((select) => {
        const selectAndDispatchChange = (option) => {
            if (!option) return;
            select.value = option.value;
            select.dispatchEvent(new Event("change"));
        };

        // Check if there are any options matching the incoming configs
        objectSwitchers.forEach((os, _key) => {
            const optionToSelect = Array.from(
                select.options
            ).find(
                (option) => option.value === os.active_object
            );
            selectAndDispatchChange(optionToSelect);
        });

        materialSwitchers.forEach((ms) => {
            const optionToSelect = Array.from(
                select.options
            ).find(
                (option) => option.value === ms.active_material
            );
            selectAndDispatchChange(optionToSelect);
        });
    });
}
```

#### Helper functions

We use a couple of helper function to better separate logic that we reuse in the main functions:

```javascript
// We can make this function more advanced if we need
// to match with a prefix or suffix in case of more complex
// models/configurations
#stateMatches(inputName, stateName) {
    return stateName === inputName;
}

// This function is a helper used to loop through the current
// configs, and update them so we can apply the changes from the UI
#loopConfigs(currentConfigs, newConfigs, key, value, options) {
    for (const config of currentConfigs) {
        // We delete these properties since we are reusing the current configs
        delete config["active_material_instanceId"];
        delete config["object_instanceId"];
        delete config["active_object_instanceId"];
        delete config["variant_instanceId"];

        if (!(key in config)) continue;

        const prevOption = options.find((option) =>
            this.#stateMatches(option.value, config[key])
        );
        if (!prevOption) continue;

        if (value === config[key]) continue;
        newConfigs.push({
            ...config,
            [key]: value,
        });
    }
}
```

### 2.4. All together

{% embed url="https://codesandbox.io/embed/custom-eshop-integration-6w5ldd?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="false" %}

Remember that this example is for when you are using select. You will need to adapt the code to retrieve the information from whatever other HTML structure you are using in your site.





## PDF Generation



At some point, you may want your clients to be able to download a PDF of the current product’s configuration. Here’s an example on how you could start approaching such thing using the popular [https://github.com/parallax/jsPDF](https://github.com/parallax/jsPDF) library:

You can test how it works here:[https://mqxld9.csb.app](https://mqxld9.csb.app)

{% embed url="https://codesandbox.io/p/sandbox/pdf-generation-mqxld9" fullWidth="true" %}

