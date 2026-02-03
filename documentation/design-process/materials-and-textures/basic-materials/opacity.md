# Opacity

Adjusts the transparency of a material. A value of 100 makes the material fully opaque, while lower values make it more transparent.&#x20;

A black-and-white opacity texture can be imported, where black represents full transparency and white represents full opacity.<br>

Opacity supports two blending modes: **Blend** and **Mask:**

* **Blend** provides smooth transitions between transparent and opaque areas
* **Mask** works on a binary principle, meaning it does not produce intermediate transparency levels like Blend mode. It is particularly **recommended for AR**, as it ensures decals and textures display correctly.\
  Using Mask mode ensures that transparent areas do cast **shadows**, unlike Blend mode, where partial transparency prevents proper shadow formation. \
  Additionally, Mask mode improves **performance** by simplifying rendering calculations.&#x20;

The **Invert** option reverses the texture colors, turning white into black and vice versa.

{% embed url="https://vimeo.com/769964397" %}

* Linear gradient — HEX, RGB
* Radial gradient — HEX, RGB
* Texture — JPG, PNG, SVG
* Animation — Lottie, GIF, MP4
* Figma frame — [figma-frames-import.md](../../../importing/figma-frames-import.md "mention")

