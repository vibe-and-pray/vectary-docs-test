---
description: Programmatic control of embedded Vectary 3D scenes via JavaScript
hidden: true
noIndex: true
---

# Model API \[new]

Vectary is designed as a no-code platform, but some scenarios - especially integration with external websites - require programmatic control. Model API provides this capability: you can connect your website to an embedded 3D model, synchronize your interface with the scene state, and respond to user actions in 3D.<br>



{% hint style="warning" %}
Available only on **Business** plans
{% endhint %}





### How it works



Vectary projects are embedded on websites via iframes. Since iframes are isolated from the parent page, communication uses the `postMessage` mechanism.

For Business plans, Vectary provides a script that can be added to your website. This script contains the `VctrModelApi` class - a wrapper around `postMessage` with convenient async methods. You create an API instance for each iframe and call methods to control the scene.

Unlike low-level libraries like Three.js or Babylon.js, most visual configuration is done in Vectary Studio without code. The API is for integration - connecting your ready-made 3D scene with your website's logic.







### Capabilities



A few examples of API capabilities (see [<mark style="color:blue;">API Reference</mark>](api-reference-new/) for the full list of methods).



{% hint style="info" %}
&#x20;Some features may be available but not yet documented - [contact us](https://www.vectary.com/contact/) if you need something specific
{% endhint %}



<table><thead><tr><th width="238.66015625">Category</th><th>Description</th></tr></thead><tbody><tr><td>Initialization</td><td>Establish connection with the embedded model</td></tr><tr><td>Configuration</td><td>Read and change active variants and materials</td></tr><tr><td>Events</td><td>Two-way communication - receive scene events (clicks, hover, state changes, and more), send data to trigger scene logic</td></tr><tr><td>Floating UI</td><td>Interact with in-scene UI elements</td></tr><tr><td>Materials</td><td>Change colors, textures, PBR properties</td></tr><tr><td>Textures</td><td>Upload images, overlay textures with positioning</td></tr><tr><td>Camera</td><td>Control position, target, field of view</td></tr><tr><td>Animations</td><td>Play, stop, seek to specific frame</td></tr><tr><td>Objects</td><td>Transformations, visibility, duplication</td></tr><tr><td>Import/Export</td><td>Load 3D models, images, export to GLB/GLTF/FBX/USDZ</td></tr></tbody></table>







### How API connects to Vectary Studio



Model API works together with settings configured in Vectary Studio. Most visual aspects are set up in the editor, while the API lets you control and modify them programmatically. Learn more about these concepts in [<mark style="color:blue;">Core Concepts</mark>](core-concepts-new.md).



<table><thead><tr><th width="197.33984375">Studio concept</th><th>Role in API</th></tr></thead><tbody><tr><td><a href="../../documentation/3d-configurator/variants.md">Variants</a></td><td>Object groups with switchable visibility - API activates the desired variant</td></tr><tr><td><a href="../../documentation/design-process/materials-and-textures/">Materials</a></td><td>Set of materials on an object - API switches the active material</td></tr><tr><td><a href="../../documentation/3d-configurator/floating-ui/">Floating UI</a></td><td>In-scene UI elements - API reads their state and responds to interactions</td></tr><tr><td><a href="../../documentation/3d-configurator/interactions/">Interactions</a></td><td>Trigger → Action logic - API sends and receives events</td></tr><tr><td><a href="../../documentation/3d-configurator/variables-and-expressions/">Variables</a></td><td>Scene variables - API reads and writes values</td></tr><tr><td><a href="../../documentation/3d-configurator/animations.md">Animations</a></td><td>Timeline animations - API controls playback</td></tr></tbody></table>







### Documentation sections



<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="image">Cover image</th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Quick Start</strong></td><td><mark style="color:$info;">Step-by-step setup - from iframe to first API call</mark></td><td><a href="../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td><td><a href="quick-start-new.md">quick-start-new.md</a></td></tr><tr><td><strong>Core Concepts</strong></td><td><mark style="color:$info;">Key concepts for understanding the API and Vectary Studio</mark></td><td><a href="../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td><td><a href="core-concepts-new.md">core-concepts-new.md</a></td></tr><tr><td><strong>API Reference</strong></td><td><mark style="color:$info;">Methods by category with signatures, examples, and types</mark></td><td><a href="../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td><td><a href="api-reference-new/">api-reference-new</a></td></tr><tr><td><strong>Ecommerce</strong></td><td><mark style="color:$info;">Patterns for online stores (Shopify, Webflow, Custom)</mark> </td><td><a href="../../.gitbook/assets/Frame 1.png">Frame 1.png</a></td><td><a href="ecommerce-new.md">ecommerce-new.md</a></td></tr></tbody></table>













