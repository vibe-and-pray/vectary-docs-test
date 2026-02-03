# Ground plane



## Overview



The Ground Plane is a virtual surface that helps integrate 3D objects into a scene by providing a base for casting shadows. It enhances realism by ensuring objects appear grounded rather than floating in space.

{% embed url="https://vimeo.com/830631279" %}

## **Dynamic shadows**



Dynamic Shadows adjust in real time based on scene lighting, ensuring accurate interaction with moving elements.



## Baked shadow



Pre-rendered shadows that remain fixed, improving performance and producing a much more photorealistic result.

Learn more about texture baking and its settings here: [baked-textures](materials-and-textures/baked-textures/ "mention")<br>

* **Black point** — controls the darkest areas of the shadow, determining how deep the shadows appear
* **White point** — adjusts the lightest parts of the shadow, influencing shadow softness and blending with the environment



## Settings



Settings in the Adjust tab apply to both Dynamic and Baked shadows:

{% tabs %}
{% tab title="Size" %}
The size of the shadow plane can be adjusted, and values greater than **2500** can be manually entered.

<figure><img src="../../.gitbook/assets/image (403).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Opacity" %}
A transparency setting allows control over shadow opacity.

<figure><img src="../../.gitbook/assets/image (404).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Color" %}
Shadow color can be modified to match the scene.

<figure><img src="../../.gitbook/assets/image (405).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Shadow intensity" %}
`Only for Dynamic` \
Shadow intensity is determined by the light source. If the shadow originates from the Environment, the 'Shadow' setting in the environment controls affects its intensity.

<figure><img src="../../.gitbook/assets/image (402).png" alt="" width="375"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

