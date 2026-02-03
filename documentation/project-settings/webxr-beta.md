# WebXR (beta)

## **Overview**



**WebXR** is an industry-standard API designed to enable immersive experiences directly within web browsers, encompassing both Virtual Reality (VR) and Augmented Reality (AR). "WebXR" stands for "Web Extended Reality", where "XR" refers collectively to all immersive technologies, including VR, AR, and Mixed Reality (MR).



## How to add WebXR to a project



To activate **WebXR**, open the right-hand panel, go to the **Advanced** section, select WebXR, configure the settings as needed, and publish the project via Share.

<figure><img src="../../.gitbook/assets/image (44).png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="success" %}
#### WebXR + AR

Enabled [**Augmented Reality**](augmented-reality-webar.md) will not conflict with WebXR. If a device supports WebXR, a trigger icon for entering WebXR will be displayed; if not, a trigger icon for AR will be shown.
{% endhint %}





## Settings



{% hint style="warning" %}
#### Updating settings for WebXR

After modifying WebXR settings, make sure to update the entire project via the Share settings.

![](<../../.gitbook/assets/image (43).png>)
{% endhint %}



{% tabs %}
{% tab title="Trigger" %}
<div align="left"><figure><img src="../../.gitbook/assets/image (45).png" alt="" width="375"><figcaption></figcaption></figure></div>

`1` - show or hide the WebXR icon

`2`  - select the corner position for the WebXR icon

**`3`** - **padding:** define the spacing for the WebXR icon

**`4`** - **width:** set the size of the WebXR icon

**`5`** - upload a custom image to be used as the icon for entering the WebXR experience (PNG or JPG)

`6` - upload a custom image to be used as the icon for exiting the WebXR experience (PNG or JPG)

Entry into WebXR experience can be triggered by any 3D object or UI element using the [WebXR action](../3d-configurator/interactions/actions/webxr-action.md).
{% endtab %}

{% tab title="Behavior" %}
<div align="left"><figure><img src="../../.gitbook/assets/image (541).png" alt="" width="375"><figcaption></figcaption></figure></div>

**`7`** - **Allow scaling -** activate to allow object scaling within the WebXR experience

**`8`** - **Units** - define [units](../getting-started/units.md) of measurement for WebXR model

**`9`** -  **Scale factor -** this setting allows adjusting how large or small the model appears in WebXR without changing its original size. For example, **500%** makes the object **5× larger**, while **50%** makes it **2× smaller**.
{% endtab %}
{% endtabs %}





## **Key differences between WebXR and other AR solutions**



* **Augmented Reality (AR)**: Uses a device's camera to overlay virtual objects onto the real world (passthrough mode). Primarily used with smartphones and AR headsets.
* **Virtual Reality (VR)**: Creates a completely virtual environment without using a camera. Primarily utilized with VR headsets.
* **Extended Reality (XR)**: A general term covering both AR and VR experiences.



## **Comparison with current AR solution**



Our decision to adopt WebXR is driven by limitations observed in current AR solutions:<br>

* **Direct File Display**: Current AR solutions require processing and sending **GLB** or **USDZ** files to devices, causing potential delays. WebXR eliminates this conversion, enabling faster previews.
* **Interactivity**: Current AR solutions support only basic animation (typically limited to the first animation) and lack interactive features such as hotspots and floating UIs.
* **Rendering Engine**: Variability in rendering engines for existing AR solutions can result in inconsistent visual outcomes. WebXR provides consistent rendering across operating systems.
* **Performance**: WebXR demands more rigorous optimization of projects compared to traditional AR solutions.



## **Current state of WebXR (beta) in Vectary**



WebXR currently supports:<br>

* Interactive elements
* Animations
* Floating UIs and Hotspots (currently available only on Android devices; unsupported on VR headsets)





## **Device Compatibility**



WebXR is currently fully supported on:<br>

* **Android devices**
* **VR/AR headsets** including Meta Quest 2, 3, Pro, HTC XR Elite, and Apple Vision Pro (VR mode only)<br>

Limited support is available for:<br>

* **iOS devices**: Requires specialized WebXR-compatible browsers such as [XR Browser](https://apps.apple.com/us/app/xr-browser/id1588029989) (_experimental; occasional bugs possible_)





## **Future direction**



We aim to maintain dual support for existing AR solutions and WebXR, particularly until Apple enhances WebXR compatibility, ensuring broader device coverage and stability.



## **Integration and usage**



* **Activating WebXR**: Enable WebXR via the right-hand panel by selecting **Advanced** > **WebXR (beta)**.
* **Coexistence**: WebXR integrates alongside existing AR experiences, allowing simultaneous use within the same project.
* **Device-Specific Buttons**: Buttons to activate WebXR appear only on supported devices.



## Example



Try it here: [https://app.vectary.com/p/5RIkiwHv7UDqJiECo5nxhR](https://app.vectary.com/p/5RIkiwHv7UDqJiECo5nxhR)





## **Conclusion**



WebXR significantly advances the immersive and interactive browser-based experience. Despite current limitations and partial support on iOS, WebXR provides faster performance, enhanced interactivity, and extensive support across various VR/AR devices. Continued development will enhance compatibility and user experience for both current AR implementations and WebXR.



