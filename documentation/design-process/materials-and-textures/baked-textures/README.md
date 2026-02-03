# Baked textures

## Overview



Texture Baking is the process of storing calculated rendering information onto a texture (image). This process can be performed for individual objects or multiple objects simultaneously.

#### **Benefits**

* Performance\
  \
  Texture baking allows disabling the Ambient Occlusion effect and significantly reduces or eliminates the necessity for real-time lighting calculations. As a result, overall rendering performance improves noticeably.<br>
* Realism\
  \
  The photorealistic path-tracing rendering method utilized by texture baking ensures highly realistic and impressive visual outcomes.



{% hint style="success" %}
Texture baking calculations are performed locally on the computer, fully leveraging **CPU** capabilities
{% endhint %}





## **What textures can be baked in Vectary Studio**



<table><thead><tr><th width="260.83984375">Textures</th><th>Description</th></tr></thead><tbody><tr><td><a data-mention href="ambient-occlusion-texture.md">ambient-occlusion-texture.md</a></td><td>A grayscale texture that simulates soft shadowing and ambient light occlusion in crevices and tight spaces, enhancing the realism of 3D models by adding depth and detail to surfaces.</td></tr><tr><td><a data-mention href="lightmap.md">lightmap.md</a></td><td>A precomputed texture that stores lighting data, enhancing visual realism and optimizing.</td></tr><tr><td><a href="../../ground-plane.md#baked-shadow">Ground plane</a></td><td>A virtual surface that helps integrate 3D objects into a scene by providing a base for casting shadows.</td></tr><tr><td><a data-mention href="texture-remapping.md">texture-remapping.md</a></td><td>Converting <strong>AO map</strong> and <strong>Lightmap</strong> textures into <strong>Roughness</strong> and <strong>Emission</strong> to ensure proper functionality across all devices in AR.</td></tr></tbody></table>





## Settings



Optimal settings vary significantly depending on each object's characteristics and scene context, including object dimensions, material properties, lighting setup, and visibility within the scene. It is recommended to initially choose lower settings and gradually increase these parameters if necessary.



#### Resolution

* Available resolutions: 256px, 512px, 1024px, 2048px, 4096px
* Auto mode dynamically determines optimal texture resolution based on the size of objects relative to the largest one in the scene.



#### **Quality**

This parameter determines the number of samples used during rendering. The higher the sample count, the longer the rendering process takes, but the smoother the final texture.

* Draft: 16 samples
* Medium: 256 samples
* High: 1024 samples



#### **Denoise**

Removes visual noise from baked textures, improving clarity.





## UV0 & UV1



UV channels define how textures are projected onto 3D models by mapping 2D image data onto 3D geometry. Effective UV mapping is essential for accurate texture representation. Vectary Studio supports two distinct UV channels for optimized texture baking workflows.<br>

<figure><img src="../../../../.gitbook/assets/image (258).png" alt="" width="563"><figcaption><p><strong>Ambient Occlusion</strong> map and <strong>Lightmap</strong> are generated as <strong>UV1</strong> by default, but can be set to become part of <strong>UV0</strong></p></figcaption></figure>

{% tabs %}
{% tab title="UV0" %}
* Use this channel to link Ambient Occlusion and Lightmap textures with other textures (Color, Roughness, Metalness, etc.). This allows all linked textures to update simultaneously when adjusting texture projection.
* Beneficial if the model was already UV unwrapped prior to importing into Vectary.



**Textures using UV0:**

* Color
* Roughness
* Metalness
* Opacity
* Emission
* Normal map
* Thickness

<div align="left"><figure><img src="../../../../.gitbook/assets/image (394).png" alt="" width="188"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="UV1" %}
* Use this channel to keep Ambient Occlusion and Lightmap textures independent from other textures.
* Matches the object's exact geometry, thus requiring proper UV unwrapping for accurate results.\
  ![](<../../../../.gitbook/assets/image (395).png>)
* Slightly increases the scene size due to an extra UV map.



**Textures using UV1**:

* Ambient Occlusion
* Lightmap
{% endtab %}
{% endtabs %}

{% hint style="info" %}
It is generally preferable to maintain **UV0** and **UV1** separately, ensuring independent adjustments of the texture projection
{% endhint %}

* **Update UV** — necessary when geometry is altered to ensure textures correctly align with the updated geometry.



> **Example:**
>
> A 3D table model includes two textures: a wood texture (Color, UV0) and a Lightmap (UV1). If the projection of the wood texture (UV0) needs adjusting, it can be done independently, without affecting the Lightmap texture on UV1.





## **Baking time**



Texture baking, based on path tracing, produces high-quality results but takes time. Baking duration depends on resolution, sample quality, and the number of objects.

\
Optimizing baking time:

* Begin with lower resolutions for testing
* Limit resolution and sample settings to practical necessities
* Bake smaller object groups or individually
* Temporarily hide non-essential objects
* Utilize real-time Lightmap previews for quicker assessments

{% hint style="success" %}
Continue working on the scene during baking
{% endhint %}





## Common issues



Artifacts (Fireflies): Bright spots may appear on textures due to highly reflective or refractive materials acting as secondary light sources.

Elimination methods:

* Adjust lighting intensity or reduce the number of lights.
* Lower reflectivity or increase roughness in material settings.
* Raise quality (sample count).
* Enable Denoise to minimize or remove artifacts.





## Tutorials



{% embed url="https://youtu.be/mRqP08zpbBU" %}

{% embed url="https://www.youtube.com/watch?v=B7fproJakQU" %}



