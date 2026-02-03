# Augmented Reality (WebAR)

## Overview



The current Augmented Reality (AR) functionality leverages native AR frameworks available on mobile devices - specifically **ARCore** for Android and **ARKit** for iOS. It is supported on compatible Android and iOS devices and launches directly via built-in AR applications, eliminating the need to download additional apps.

This implementation supports animations, although with some restrictions. It currently does not support [interactions](../3d-configurator/interactions/) or [UI elements](../3d-configurator/floating-ui/) within the AR environment.

Development efforts are actively focused on [webxr-beta.md](webxr-beta.md "mention"), which is currently accessible in beta. WebXR aims to provide a complete AR experience, including interactive UI, advanced materials, realistic lighting, and interactive elements identical to those in the Studio.





## How to add AR (+ QR code)



To add AR to a project:



1. Enable the AR feature using the right-hand panel.
2. A configuration window will appear, initiating the generation of two files (**GLB** for **Android** and **USDZ** for **iOS**).
3. Once file generation is complete, <mark style="color:green;">green checkmarks</mark> will indicate successful creation.

<div align="left"><figure><img src="../../.gitbook/assets/image (449).png" alt="" width="375"><figcaption></figcaption></figure></div>

Now you can open the preview mode to confirm the AR icon has been successfully added to the project. This AR icon activates the AR experience automatically on mobile devices or displays a **QR code** for desktop users to scan.&#x20;

Entry into AR mode can also be configured differently — through interaction with any 3D object or [UI element](../3d-configurator/floating-ui/). To do this, create an interaction in [Interact mode](../3d-configurator/interactions/) using a [trigger](../3d-configurator/interactions/triggers.md) and [AR](../3d-configurator/interactions/actions/ar-action.md) action.

<figure><img src="../../.gitbook/assets/ar.gif" alt=""><figcaption></figcaption></figure>



## Settings



{% hint style="warning" %}
#### Updating settings for AR

After modifying AR settings, make sure to update the entire project via the Share settings.

![](<../../.gitbook/assets/image (43).png>)
{% endhint %}



{% tabs %}
{% tab title="Source" %}
<div align="left"><figure><img src="../../.gitbook/assets/SCR-20250520-pzwz-2.png" alt="" width="375"><figcaption></figcaption></figure></div>

**`1`** - <img src="../../.gitbook/assets/image (452).png" alt="" data-size="line">  to generate/update AR files

**`2`** - <img src="../../.gitbook/assets/image (451).png" alt="" data-size="line">  indicates the project has been successfully generated

**`3`** - <img src="../../.gitbook/assets/image (453).png" alt="" data-size="line">  for uploading a file directly into AR, ignoring current scene content

**`4`** - specify object or [selection](../other/selections.md) to generate for AR (other objects will be ignored)\
\
**GLB** file for **Android**\
**USDZ** file for **iOS**
{% endtab %}

{% tab title="Trigger" %}
<div align="left"><figure><img src="../../.gitbook/assets/image (40).png" alt="" width="375"><figcaption></figcaption></figure></div>

**`5`** - show or hide the AR icon

`6`  - select the corner position for the AR icon

**`7`** - **padding:** define the spacing for the AR icon

**`8`** - **width:** set the size of the AR icon

**`9`** - upload a custom image for the AR icon (PNG or JPG)\
\
Entry into AR experience can be triggered by any 3D object or UI element using the [AR action](../3d-configurator/interactions/actions/ar-action.md).<br>
{% endtab %}

{% tab title="Behavior" %}
<div align="left"><figure><img src="../../.gitbook/assets/image (2).png" alt="" width="563"><figcaption></figcaption></figure></div>

**`10`** - **Units** - define [units](../getting-started/units.md) of measurement for generated AR files

**`11`** - **Scale factor -** this setting allows adjusting how large or small the model appears in AR without changing its original size. For example, **500%** makes the object **5× larger**, while **50%** makes it **2× smaller**.

**`12`** - **Allow scaling** - activate to allow object scaling within the AR experience

**`13`** - **Show current configuration** - if activated, modified project configurations automatically apply to AR

**`14`** - **Language** - select language displayed below the QR code (`auto` selects based on user's language settings)
{% endtab %}
{% endtabs %}



### Show current configuration



This function is enabled by default in AR settings, allowing AR files to automatically update when the end user makes changes in the configurator. If the end user modifies an object's color or configuration, activating AR will automatically generate a new file reflecting the user's selections.

<figure><img src="../../.gitbook/assets/image (176).png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="warning" %}
Please note that this feature does not function in Preview mode. To test its functionality, the project must be shared and opened separately via the provided link.
{% endhint %}



{% embed url="https://www.youtube.com/watch?v=_RhZDHPfJms" %}



## Animations



The current AR implementation supports animation, but with some restrictions due to the inherent limitations of ARCore and ARKit:



* Only animations from the first tab in the Animate mode will play in AR (keyframes from other tabs can be moved to the first tab)
* Animations in AR always play in repeat mode
* Animations cannot be stopped
* Animation playback begins even before the object is placed in the real world





## Materials



* Not all materials are supported in AR.
* Some materials may appear differently on Android and iOS devices.
* Supported materials include:
  1. All basic properties (**Color**, **Roughness**, **Metalness**, **Opacity**, **Emission**, **Normal map**) and their textures
  2. Refraction
  3. To ensure correct display of textures such as **Ambient Occlusion** and **Lightmap**, use the [Texture Remapping](../design-process/materials-and-textures/baked-textures/texture-remapping.md) feature, which converts these textures into supported textures.<br>

{% hint style="warning" %}
[Double-sided](../design-process/materials-and-textures/advanced-materials/double-sided-material.md) materials are not supported on iOS.\
\
Solution: duplicate a geometry and [flip the normals](../design-process/edit-mode/normals.md) in [edit mode](../design-process/edit-mode/).
{% endhint %}



## Tutorials



{% embed url="https://youtu.be/u25b3hw4vnI?si=y1o2WL34Cp-cyrDj" %}

