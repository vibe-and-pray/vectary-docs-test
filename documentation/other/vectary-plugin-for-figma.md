---
description: Meet the new plugin for Figma
---

# Vectary Plugin for Figma



## Overview



The Vectary plugin for Figma enables seamless integration of 3D projects into Figma workflows. It allows applying designs to 3D models, real-time fitting on the canvas, exporting high-quality renders, and accessing AR features directly within Figma.



#### Key Capabilities



* Apply design to a 3D project with just two clicks
* Real-time 3D model fitting on the canvas using Preview mode
* Export rendered image to the Figma canvas
* Immediate texture reflection in AR (AR can be activated from Figma)
* Save all applied textures for use in configurators without altering the original project
* Quickly open a 3D project in Figma with interactions, animations, AR, and UI elements
* Modify existing project textures
* Change background (including transparent option)
* Add a shadow to the scene





## Getting started

\
No tokens are required. A Vectary project link is sufficient to begin.

Upon launching the plugin, a field appears for pasting a Vectary project link, along with options to load demo projects.

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

#### Loading a 3D Project

\
**Option 1:** use demo projects\
\
Select one of the available demos and start working immediately.

\
**Option 2:** use a custom Vectary project<br>

1. Sign up on the [Vectary platform](https://www.vectary.com/)
2. Create a new project
3. [Share](../sharing-exporting-embedding/sharing.md) the project and copy the link
4. Paste the link into the plugin

{% hint style="success" %}
When a custom project is loaded, all configurations (interactions, animations, AR, Floating UI) will remain functional.
{% endhint %}





## Features



<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>



### Material picker



Enables applying a Figma frame to a material selected from a 3D object.

<div align="left"><figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure></div>

**How to use:**<br>

1. Select the Material Picker tool
2. Use the dropper to hover over and select a material (material name appears near cursor)
3. Once selected, the material name appears next to the dropper icon
4. Click on a Figma frame to apply the selected material

{% embed url="https://screen.studio/share/qHuMwVrJ" %}



### Get material frame from object



Exports the object's texture as a frame to the Figma canvas.

* Only the [**Color**](../design-process/materials-and-textures/basic-materials/color.md) texture is exported (Opacity, Emission, Normal maps are not included)
* If the texture was replaced using the Material Picker, the original texture will still be used for export

<div align="left"><figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure></div>



**How to use:**<br>

1. Select the Get Material Frame from Object tool
2. Hover over the object to reveal the material name
3. Click to extract the texture
4. A Figma frame with the texture will appear on the canvas

{% embed url="https://screen.studio/share/iXrYbN5b" %}



### Ground shadow



Activates the [ground plane](../design-process/ground-plane.md), which can be further customized in the Vectary Studio.

<div align="left"><figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure></div>





### Background



Allows enabling/disabling the background. A transparent background is available.

<div align="left"><figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Note: Background color is affected by the [Adjustment effect](../design-process/effects/adjustments.md).
{% endhint %}





## Preview&#x20;



Enables real-time model preview within the Figma frame.<br>

* Preview quality is low for performance; high-quality image is generated during export
* Requires use of **Create Image** to activate
* Preview Mode is disabled automatically after creating or updating an image
* Plugin is linked to a single frame; for multiple instances, duplicate the frame

{% embed url="https://screen.studio/share/68JWQcth" %}



## Create image - Update image



* **Create Image**: Captures the current project view and creates a frame on the canvas

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

* **Update Image**: Refreshes an existing plugin-generated frame with current model view

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>





## Reopen Plugin&#x20;



The plugin retains memory of existing frames and associated settings.

\
**Two reopen scenarios:**<br>

1. **Frame selected**: Plugin reopens the same project, preserving view and settings (including texture/configurator changes)
2. **No frame selected**: Plugin starts a new session and creates a new frame upon image creation





## Tutorials



{% embed url="https://youtu.be/TcCeKi2KBZM?si=V7TtohP8T4GlnlJZ" %}

