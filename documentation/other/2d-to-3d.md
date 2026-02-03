---
description: Turn SVG into 3D with a couple of clicks
---

# 2D to 3D



{% hint style="success" %}
#### AI-based 3D model generation from image

Learn more about AI-based 3D model generation here: [image-to-3d-model](image-to-3d-model/ "mention")
{% endhint %}



## Overview



To transform a 2D image into 3D, it must be in SVG (vector) format.

Once an SVG file is prepared, it can be imported by simply dragging and dropping it onto the canvas. After import, thickness can be set and the object can be converted into a geometric element.

{% embed url="https://vimeo.com/728847812" %}



## Post-import settings for SVG objects



* Texture Size - if the SVG object is intended to be converted into a plane, the resolution for the texture can be predefined. This setting can also be adjusted later in the material properties.<br>
* Segments - Controls the level of detail in the object when converting it into geometry (mesh). Increasing or decreasing the number of segments changes the polygon count and surface smoothness.<br>
* Offset - Defines the spacing between layers in a multi-layered SVG. Default offset is 1, preventing visual blending between layers by placing them on slightly different levels.<br>
* Extrude - Sets the thickness of the object. Thickness and other parameters can be adjusted at any time after conversion.<br>

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="365"><figcaption></figcaption></figure>



## Conversion options



### Convert to Plane



Transforms the SVG into a flat surface with textures applied. This process is similar to importing standard image files (PNG, JPG).



### Convert to Geometry



Converts the SVG into a geometric object or multiple objects, depending on the number of layers in the original SVG.

Right-click on the SVG object in the canvas or in the left panel and choose the geometry conversion option



<figure><img src="../../.gitbook/assets/image (456).png" alt="" width="375"><figcaption></figcaption></figure>



