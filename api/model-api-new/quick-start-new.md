---
description: Get the Model API running with your embedded Vectary project in 5 minutes.
---

# Quick Start \[new]



### Prerequisites



* Vectary project (create one at [vectary.com](https://www.vectary.com))
* **Business** plan
* Basic knowledge of HTML and JavaScript







{% stepper %}
{% step %}
### Step 1: Get your Project ID





* Open your project in Vectary Studio
* Click **Share** in the top right corner
* Copy the **Project ID** from the embed URL:

```
https://app.vectary.com/p/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
                          └──────────── Project ID ────────────┘
```


{% endstep %}

{% step %}
### Step 2: Add the embed to your page





Create an HTML file with an iframe pointing to your project:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Vectary API Demo</title>
</head>
<body>
  <iframe 
    id="vectary-embed"
    src="https://app.vectary.com/p/YOUR_PROJECT_ID"
    width="800" 
    height="600"
    frameborder="0"
  ></iframe>
</body>
</html>
```

Replace `YOUR_PROJECT_ID` with the ID from **Step 1**


{% endstep %}

{% step %}
### Step 3: Initialize the API





Add this script after the iframe:

```html
<script type="module">
  import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";

  // Create API instance with the iframe's DOM id
  const api = new VctrModelApi("vectary-embed");
  
  // Wait for initialization
  await api.init();
  
  console.log("API ready!");
</script>
```

Open your browser's console - you should see "API ready!" once the model loads.


{% endstep %}

{% step %}
### Step 4: Make your first API call





The API provides many methods to control the scene (see the full list in the [<mark style="color:blue;">API Reference</mark>](api-reference-new/)). Here's a simple example to get you started:

```html
<script type="module">
  import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";

  const api = new VctrModelApi("vectary-embed");
  await api.init();

  // Get all objects in the scene
  const objects = await api.getObjects();
  console.log("Scene objects:", objects);
</script>
```



#### Complete example

Here's a full working example that lists all objects in the scene:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Vectary API Demo</title>
  <style>
    body { font-family: sans-serif; padding: 20px; }
    iframe { border: 1px solid #ccc; }
    pre { background: #f5f5f5; padding: 15px; overflow: auto; }
  </style>
</head>
<body>
  <h1>My 3D Configurator</h1>
  
  <iframe 
    id="vectary-embed"
    src="https://app.vectary.com/p/YOUR_PROJECT_ID"
    width="800" 
    height="600"
    frameborder="0"
  ></iframe>

  <h2>Scene Objects</h2>
  <pre id="output">Loading...</pre>

  <script type="module">
    import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";

    const api = new VctrModelApi("vectary-embed");
    await api.init();

    const objects = await api.getObjects();
    document.getElementById("output").textContent = JSON.stringify(objects, null, 2);
  </script>
</body>
</html>
```
{% endstep %}
{% endstepper %}



### Key points



<table><thead><tr><th width="281.74609375">Point</th><th>Details</th></tr></thead><tbody><tr><td>One API instance per iframe</td><td>If you have multiple embeds, create a separate <code>VctrModelApi</code> for each</td></tr><tr><td>All methods are async</td><td>Always use <code>await</code> or <code>.then()</code> - methods return Promises</td></tr><tr><td>Initialize before calling methods</td><td>Wait for <code>api.init()</code> to complete before making other calls</td></tr><tr><td>Error handling</td><td>Errors reject the Promise with <code>{ status: "error", error?: string }</code></td></tr></tbody></table>







### Troubleshooting



<mark style="background-color:$info;">**API not initializing?**</mark>



* Check that the iframe `id` matches the string passed to `VctrModelApi()`
* Ensure the project is published and accessible
* Verify your workspace has a Business plan



<mark style="background-color:$info;">**Methods returning empty results?**</mark>



* Make sure `init()` has completed before calling other methods
* Check the browser console for error messages



<mark style="background-color:$info;">**CORS errors?**</mark>



* The API script must be loaded from `app.vectary.com`, not copied locally





### Next steps



* [<mark style="color:blue;">**Core Concepts**</mark>](core-concepts-new.md) - understand Variants, Materials, Events, and Variables
* [<mark style="color:blue;">**API Reference**</mark>](api-reference-new/) - explore all available methods
* [<mark style="color:blue;">**Ecommerce**</mark>](ecommerce-new.md) - see integration patterns for online stores





