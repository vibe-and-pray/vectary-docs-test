# Importing own textures



## Overview



Vectary Studio allows importing custom textures into almost every material property, providing extensive customization options to enhance visual fidelity and achieve desired effects.

<figure><img src="../../../.gitbook/assets/image (94).png" alt="" width="563"><figcaption></figcaption></figure>



### Material properties supporting custom texture import



* [color.md](basic-materials/color.md "mention")
* [roughness.md](basic-materials/roughness.md "mention")
* [metalness.md](basic-materials/metalness.md "mention")
* [opacity.md](basic-materials/opacity.md "mention")
* [emission.md](basic-materials/emission.md "mention")
* [normal-map.md](basic-materials/normal-map.md "mention") (images imported here will automatically convert to a normal map)
* [ambient-occlusion-texture.md](baked-textures/ambient-occlusion-texture.md "mention")
* [lightmap.md](baked-textures/lightmap.md "mention")
* Thickness or [refraction.md](advanced-materials/refraction.md "mention")
* [reflectivity.md](advanced-materials/reflectivity.md "mention")



### Methods for importing textures



* Upload directly from a computer
* Insert a URL link to an image
* Import directly from Figma - [figma-frames-import.md](../../importing/figma-frames-import.md "mention")



### Supported texture formats



* Static images: **JPG**, **PNG**, **WebP, SVG**
* Animated textures: **Lottie**, **GIF**, **MP4**



### Texture management



* Imported textures remain available for use within the current project and will automatically be removed upon reopening if not applied to any material/setting.
* Imported animated textures automatically loop when the scene loads, playback can be managed in Interact mode - [animated-texture.md](../../3d-configurator/interactions/actions/animated-texture.md "mention")
* Imported textures can be modified with various controls such as **saturation**, **brightness**, **contrast**, **inversion**, **tiling**, **offset**, **rotation**, and **resolution** adjustments.

{% hint style="success" %}
All used textures and their resolutions are displayed in preview mode, enabling quick optimization
{% endhint %}





## Texture Projection



Texture projection determines how a texture maps onto the surface of a 3D object. Several projection types are available, each suited to different geometric shapes or visual effects:

<figure><img src="../../../.gitbook/assets/image (95).png" alt="" width="242"><figcaption></figcaption></figure>

* **Plane projection:** projects textures onto objects as if projected from a flat plane
* **Box projection:** applies textures onto objects using box-shaped projections
* **Sphere projection:** maps textures around an object as if wrapped around a sphere
* **Cylindrical projection:** wraps textures around cylindrical-shaped objects
* **Unwrap:** utilizes object's UV unwrap to accurately map textures according to geometry

{% hint style="success" %}
Clicking the projection shape icon repeatedly cycles through different projection axes
{% endhint %}



Manual adjustment of texture projection:

* Click the projection icon to enter texture projection editing mode
* In this mode, a Gizmo tool allows manual adjustments, including moving, scaling, and rotating textures directly on the object
* Once adjustments are complete, click the **`Exit texture projection`** button to finish editing

{% embed url="https://vimeo.com/724808402" %}







