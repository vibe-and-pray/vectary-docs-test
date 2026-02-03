---
icon: code
---

# Model API

While the Vectary platform is designed to create a no-code experience, certain advanced features -especially those involving integration with external sites - require code-level customization. The Model API enables this level of control, allowing deeper interaction with embedded 3D models.



## How it works



Vectary embeds are implemented using [iframes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) which means they operate in an isolated environment. To interact with them, a [messaging layer](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) must be used.&#x20;

For workspaces with a [Business and Grow plan](https://www.vectary.com/pricing/), Vectary provides a `script` that can be added to a website. This script includes the necessary messaging layer, enabling seamless communication with the embedded model.

Once configured, an instance of the Vectary Model API can be created for each model. These instances provide access to a set of methods for interacting with the 3D model.

Refer to the [**Quick Start**](quick-start.md) section to begin setup.



## Capabilities



The Model API allows interaction with Vectary embeds on a web page using a limited but powerful set of methods. Unlike general-purpose libraries like Three.js or Babylon.js, most model behaviors and configurations can be handled directly in Vectary Studio, minimizing the need for code.



#### Available features include:



* Initializing communication with embedded models
* Sending and receiving view data
* Sending and listening to events triggered within the 3D scene
* Connecting with Floating UI elements
* Integrating with e-commerce logic





## API sections



[quick-start.md](quick-start.md "mention")

[api-reference](api-reference/ "mention")

[type-definitions.md](type-definitions.md "mention")

[events-and-listeners.md](events-and-listeners.md "mention")

[floating-ui.md](floating-ui.md "mention")

[ecommerce](ecommerce/ "mention")





