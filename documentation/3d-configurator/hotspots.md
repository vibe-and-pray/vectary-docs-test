# Hotspots



**Hotspots** are 2D interface elements that can be anchored to any point on a 3D object or within the scene. They serve as visual triggers for executing actions, such as toggling UI elements, starting animations, or launching interactions. Behavior is defined through [**Interact mode**](interactions/).

Hotspots are always camera-facing, maintaining clear visibility from any viewing angle.



<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

Supported content types:<br>

* Static images (JPG, PNG, SVG)
* Animated assets (GIF, MP4, Lottie)
* [figma-frames-import.md](../importing/figma-frames-import.md "mention")



To anchor a Hotspot to a specific surface of a 3D object, enable the **Snap to Face** option.

{% embed url="https://screen.studio/share/IJ1yePoV" %}



#### Settings



* **Size** — sets the default display size of the Hotspot
* **Hover Size** — sets the size of the Hotspot on hover
* **Fade** — adjusts the transparency of the Hotspot when obstructed by geometry:
  * **100%** — always fully visible, even behind geometry
  * **0%** — fully hidden when occluded by geometry



