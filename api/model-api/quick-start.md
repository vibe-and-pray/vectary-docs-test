---
description: How to start using our API on one of the embedded models on your site.
---

# Quick Start

## The Basics



To begin using the API with an embedded model:



1. Import the API as a module.
2. Create an API instance and pass the DOM `id` of the `iframe` containing the embed (**`web component`** coming soon).
3. Wait for the instance to initialize.
4. Use the available methods to interact with the model.



{% hint style="info" %}
A new API instance is required for each embedded model.
{% endhint %}



{% embed url="https://codesandbox.io/embed/init-00jr7l?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}



## Async Methods



All API communication is handled using [`postMessage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/postMessage) events. As a result, all methods return Promises.





## Errors



Errors returned by API methods reject the corresponding Promise. Rejection includes a standardized error format for consistent handling.

```typescript
{
    status: "error",
    error?: string
}
```



## Init

{% content-ref url="api-reference/init.md" %}
[init.md](api-reference/init.md)
{% endcontent-ref %}



## isReady

{% content-ref url="api-reference/isready.md" %}
[isready.md](api-reference/isready.md)
{% endcontent-ref %}



## postViewData

{% content-ref url="api-reference/projectinfo.md" %}
[projectinfo.md](api-reference/projectinfo.md)
{% endcontent-ref %}

