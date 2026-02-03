# Light sources



## Overview



By default, illumination in a scene comes from environment lighting ([environment.md](../environment.md "mention")). Local light sources provide additional illumination with defined positions and characteristics. These lights can complement environment lighting or completely replace it if environment lighting is disabled. They influence the appearance of objects by casting shadows and creating highlights.



<figure><img src="../../../.gitbook/assets/image (113).png" alt="" width="374"><figcaption></figcaption></figure>



Light sources are very easy to use and configure:

{% embed url="https://vimeo.com/721493618" %}



{% hint style="warning" %}
By default, a light source does not cast shadows; this must be enabled in the settings of each light source\
\
<img src="../../../.gitbook/assets/image (114).png" alt="" data-size="original">
{% endhint %}



{% hint style="info" %}
The intensity of each light source can be set to more than 100%\
\
![](<../../../.gitbook/assets/image (115).png>)
{% endhint %}



## **Point light**



A point light emits light in all directions from a single point in space.

{% embed url="https://vimeo.com/769631484" %}



* **Radius** – defines the size of the light source, affecting how shadows and highlights appear. A larger radius creates softer, more diffused shadows and broader highlights, while a smaller radius results in sharper shadows and more concentrated highlights.



## Spot light



A spot light emits a cone-shaped beam of light. It has a defined direction, angle, radius, and softness, allowing for precise control over illumination. \
Spotlights are commonly used for stage lighting, flashlights, and focused light effects.

{% embed url="https://vimeo.com/769641464" %}



* **Radius** – defines the size of the light source within the cone. A larger radius results in a bigger apparent source, while a smaller radius keeps the light more concentrated.<br>
* **Angle** – determines the spread of the light cone. A wider angle creates a broader beam of light, while a narrower angle focuses illumination on a smaller area.<br>
* **Softness** – controls the transition between the fully illuminated area and the outer edges of the light cone. Higher softness results in a gradual fade, whereas lower softness produces a sharper falloff.





## Directional light



A directional light simulates light coming from a distant source, such as the sun. It casts parallel rays across the scene, creating consistent lighting and shadows regardless of object positions.

{% embed url="https://vimeo.com/769684100" %}



* **Angle** – controls the spread of light rays. A smaller angle results in more focused lighting with sharper shadows, while a larger angle creates softer, more diffused shadows, simulating atmospheric scattering.





## Rectangle Light



A rectangle light is an area light source that emits light from a rectangular surface. It produces soft shadows and is useful for simulating large light panels, windows, or softbox lighting setups.

{% embed url="https://vimeo.com/769685833" %}



* **Width** & **Height** – define the physical dimensions of the light source. Larger values result in softer shadows and a more evenly distributed illumination.





## Settings



* **Intensity** – determines the brightness of the light source. This value can exceed `100%` if entered manually, allowing for higher light emission levels.\
  <br>
* **Shadow** – by default, local light sources do not cast shadows. Enable this setting to allow shadows to be visible. Note that a surface is required for shadows to appear (e.g. [ground-plane.md](../ground-plane.md "mention")).&#x20;



### **Dynamic**



1. **Non-Dynamic** mode – objects with a [Lightmap](../materials-and-textures/baked-textures/lightmap.md) do not receive diffuse reflections from the light source but still contribute to specular reflections.<br>
2. **Dynamic** mode – light influences all objects in the scene, including those with a [Lightmap](../materials-and-textures/baked-textures/lightmap.md). However, dynamic light sources are ignored when baking the Lightmap.

<figure><img src="../../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>



### **Retain AO**



1. Retain AO **disabled** – objects with an [Ambient Occlusion](../materials-and-textures/baked-textures/ambient-occlusion-texture.md) map do not receive diffuse reflections but still contribute to specular reflections.<br>
2. Retain AO **enabled** – light influences all objects in the scene, including those with an [Ambient Occlusion](../materials-and-textures/baked-textures/ambient-occlusion-texture.md) map.

<figure><img src="../../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.youtube.com/watch?v=swPzcGhtThQ" %}





