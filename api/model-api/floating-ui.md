# Floating UI

Vectary configurators can be enhanced with a [Floating UI](../../documentation/3d-configurator/floating-ui/) (FUI for short), with the ability to customize different parts displayed (text, images, links, etc)

A configurator is, at a base level, just a model that contains any number of [Variants](../../documentation/3d-configurator/floating-ui/variants-ui.md) and/or [Materials](../../documentation/3d-configurator/floating-ui/materials-ui.md).

{% hint style="info" %}
learn more about configurators here: [https://www.vectary.com/3d-configurator-maker](https://www.vectary.com/3d-configurator-maker/)
{% endhint %}



### Example

Here’s an example which loads a configurator and uses the API to:

* Listen to changes in the configurator.
* Load/save changes into the [`local storage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) of the user.
* If a configuration has been saved, it will attempt to load it.<br>

{% embed url="https://codesandbox.io/s/get-setconfigurationstate-kl0psw?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}

### Get configuration state

[getconfigurationstate.md](api-reference/getconfigurationstate.md "mention") &#x20;

### Set configuration state

[setconfigurationstate.md](api-reference/setconfigurationstate.md "mention")



