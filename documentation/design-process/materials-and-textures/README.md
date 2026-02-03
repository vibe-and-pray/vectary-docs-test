---
description: Easily create stunning photorealistic materials
---

# Materials and Textures



## Overview



Vectary provides a flexible and intuitive workflow for managing materials. Users can create custom materials by adjusting key parameters such as metalness, roughness, refraction, and emission, among many others. Additionally, textures from external sources can be imported to achieve highly detailed and realistic surface effects.

A built-in material library offers a collection of ready-to-use materials, while also allowing users to store and reuse their custom materials for streamlined project management — [materials-library.md](../libraries/materials-library.md "mention")



<figure><img src="../../../.gitbook/assets/image (96).png" alt="" width="232"><figcaption></figcaption></figure>



## Sections



<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Basic materials</strong></td><td>Core material properties such as color, roughness, metalness, opacity, emission, and normal maps</td><td><a href="../../../.gitbook/assets/SCR-20250202-rfqm.jpeg">SCR-20250202-rfqm.jpeg</a></td><td><a href="basic-materials/">basic-materials</a></td></tr><tr><td><strong>Advanced materials</strong></td><td>Additional properties like subsurface scattering, refraction, clearcoat, thinfilm for more complex material effects</td><td><a href="../../../.gitbook/assets/SCR-20250202-rfjq.jpeg">SCR-20250202-rfjq.jpeg</a></td><td><a href="advanced-materials/">advanced-materials</a></td></tr><tr><td><strong>Baked textures</strong></td><td>Precomputed ambient occlusion (AO) and lightmap (LM) textures to optimize rendering performance while preserving detailed lighting and shading.</td><td><a href="../../../.gitbook/assets/SCR-20250202-rhge.png">SCR-20250202-rhge.png</a></td><td><a href="baked-textures/">baked-textures</a></td></tr><tr><td><strong>Importing own textures</strong></td><td>Importing custom textures, including settings for texture projection and mapping adjustments.</td><td><a href="../../../.gitbook/assets/SCR-20250202-rhzy.png">SCR-20250202-rhzy.png</a></td><td><a href="importing-own-textures.md">importing-own-textures.md</a></td></tr></tbody></table>



## Settings



{% embed url="https://vimeo.com/769927403" %}



To access material settings, select an object. Once selected, the right panel will display the object's material list and material properties.



#### Material settings overview

{% tabs %}
{% tab title="Projection" %}
**Texture Projection** – adjusts how a texture is mapped onto an object. \
Learn more here: [#texture-projection](importing-own-textures.md#texture-projection "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (97).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="List" %}
**Material list** – each object can have multiple materials. A material is a collection of configured properties and textures — [#managing-materials](./#managing-materials "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (98).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Library" %}
**Material Library** – icon <img src="../../../.gitbook/assets/image (100).png" alt="library icon" data-size="line"> next to the material name opens the material library — [materials-library.md](../libraries/materials-library.md "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (99).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Basic" %}
**Basic properties** — core material properties such as color, roughness, metalness, opacity, emission, and normal maps — [basic-materials](basic-materials/ "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (101).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Advanced" %}
**Advanced options** — additional properties like subsurface scattering, refraction, clearcoat, thinfilm for more complex material effects — [advanced-materials](advanced-materials/ "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (102).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Baked" %}
**Baked textures** — precomputed ambient occlusion (AO) and lightmap (LM) textures to optimize rendering performance while preserving detailed lighting and shading — [baked-textures](baked-textures/ "mention")

<div align="left"><figure><img src="../../../.gitbook/assets/image (103).png" alt="" width="231"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Transformation" %}
**Texture transformation —** these settings apply transformations to all textures within a material. Similar settings are available in the texture settings for each property.

* Tiling - controls the repetition of a texture across a surface. Increasing the tiling value results in more repetitions within the same area.
* Offset - adjusts the position of a texture along the surface, shifting it horizontally or vertically.
* Rotation - rotates the texture around its axis, altering its orientation on the surface.

<div align="left"><figure><img src="../../../.gitbook/assets/image (105).png" alt="" width="357"><figcaption></figcaption></figure></div>
{% endtab %}
{% endtabs %}





## Managing materials



Each object can have multiple materials, each defining its own set of properties and textures. Materials can be freely added, removed, duplicated, and adjusted, allowing for comprehensive control and customization throughout the project.



### **How to add a material**

To add a new material, select an object and click the **plus** icon in the material list on the right panel.

This allows multiple materials with different settings to be assigned to a single object.

<div align="left"><figure><img src="../../../.gitbook/assets/image (407).png" alt="" width="239"><figcaption></figcaption></figure></div>

### **How to duplicate a material**

To duplicate an existing material, select an object and click the **duplicate** icon next to the material name in the material list on the right panel.

<div align="left"><figure><img src="../../../.gitbook/assets/image (408).png" alt="" width="243"><figcaption></figcaption></figure></div>

### How to copy a material from another object

To copy a material from another object, select an object and click the **eyedropper** icon in the material list on the right panel. The cursor will change to a **crosshair**, indicating that you need to click on an object in the scene to copy its material. Clicking on the object will apply the selected material to the current object.

<div align="left"><figure><img src="../../../.gitbook/assets/image (409).png" alt="" width="240"><figcaption></figcaption></figure></div>

{% embed url="https://www.youtube.com/watch?v=SvdFCoo5tAg" %}

