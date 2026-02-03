# Webflow

## Introduction



If you’ve decided to create an e-shop in Webflow, and are ready to showcase your products in 3D and AR using Vectary configurators, here’s a step-by-step guide on how to get started.

We'd like to point out that in this guide, we're using the list of products and other aspects of **Webflow's E-commerce 'Store Starter'** presets.

If you want to experiment with it, you can find it when you create a new site in a **'workspace'.**



<figure><img src="../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>



## Requirements



For integrating with `Webflow E-commerce` you will need the following:

* A workspace or team Webflow subscription:
  * Without a subscription it is not possible to add embeds into any page.





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





## Webflow setup



### 2.1. Add products

First, make sure there is at least, one product on the `E-commerce` menu.

For the purpose of covering all the possible options in this guide, we are going to use a product with `variants`.

If you are not clear on how to add variants to a product, please visit Webflow’s amazing tutorial that will guide you through the required steps.\
<br>

{% embed url="https://university.webflow.com/lesson/create-product-options-and-variants" %}

<figure><img src="../../../.gitbook/assets/image (125).png" alt="" width="327"><figcaption></figcaption></figure>

Here’s a CSV file you can import for testing:&#x20;

{% file src="../../../.gitbook/assets/Store Starter - Products.csv" %}

Here is the product that we’ll be working with that mimics what we have setup in Vectary.

<figure><img src="../../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>



### 2.2. Add an Embed



Next, go to `Pages`, then the products page, in the `E-commerce pages` section.

In this case we used Webflow’s own `Products Template`.

<figure><img src="../../../.gitbook/assets/image (127).png" alt="" width="327"><figcaption></figcaption></figure>



Next up, go to Navigator and select your Product Image.



<figure><img src="../../../.gitbook/assets/image (128).png" alt="" width="272"><figcaption></figcaption></figure>



Add the embed right inside.

<figure><img src="../../../.gitbook/assets/image (129).png" alt="" width="329"><figcaption></figcaption></figure>

The HTML Code Embed Editor will pop up. Directly paste the iframe code of any of your shared projects in the folder created. Remember to copy the code directly from the Copy embed button in Vectary’s share popup.

{% content-ref url="../../../documentation/sharing-exporting-embedding/sharing.md" %}
[sharing.md](../../../documentation/sharing-exporting-embedding/sharing.md)
{% endcontent-ref %}

Once the embed is copied, **it is very important to give it an id.** We recommend setting both the `with` and `height` in the code to `100%`.

For example, we gave it the id `vectary_embed`:

```javascript
<iframe 
	id="vectary_embed" 
  src="https://app.vectary.com/p/{shared_model_id}" 
  frameborder="0" 
  width="100%" 
  height="100%">
</iframe>
```

Do not worry if the model you added does not match the current selected product in the editor. As we mentioned before, we were setting up Awesomeness but currently we have another product selected.

<figure><img src="../../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>



### 2.3. Add an id to the product name element

For loading the correct model, the integration needs to know which element in your shop holds the name of the product.

In this case, it is in the Heading 1 of the Product content wrapper.

<figure><img src="../../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

It has the id `product_name`. Make sure to get the text from the product’s name.

<figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

### 2.4. Add the script of the integration

The last step is to go to the Projects settings and into the Custom Code section. Add the following script to the Footer Code.

{% embed url="https://university.webflow.com/lesson/custom-code-in-the-head-and-body-tags#footer-code" %}

```javascript
<script type="module">
    import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";
    var modelApi = new VctrModelApi("vectary_embed");
    await modelApi.setWebflowEcommerce("{folder_id}", "product_name");
</script>
```



#### What the script is doing exactly?



1. Import our `VctrModelApi`
2. Create a new instance of the API, linking to the embed we created before, with the `iframe id` we set in step \*\*#2.2 (\*\*e.g. `vectary_embed`).
3. Set the integration with our `{folder_id}` from step **#1.1** and the `product name element id` from step **#2.3** (e.g. `product_name`). Before proceeding please check the following:\
   \
   a. If you are using the default Add to cart element you are good to go. \
   \
   &#x20;    ![](<../../../.gitbook/assets/image (133).png>)\
   \
   b. If you are using your own custom layout to display how the users select your product variants, there is the option to add a 3rd parameter to the setWebflowEcommerce function, where you can enter a [CSS selector](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors) of a parent element from those options, so the integration can find them.

<figure><img src="../../../.gitbook/assets/image (134).png" alt="" width="241"><figcaption></figcaption></figure>



### 2.5 Save and Publish



That’s it! By following these steps it is possible to set up an interactive 3D product configurator in no time.

{% embed url="https://store-starter-c51302.webflow.io/product/awesomeness" %}
