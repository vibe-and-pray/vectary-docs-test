# Environment

## Overview



Environment in 3D scenes defines the lighting and reflections of the scene. This is achieved using an **HDRI** (High Dynamic Range Image), which provides realistic lighting by capturing a wide range of luminance values, from deep shadows to bright highlights. The lighting in your scene primarily comes from this HDRI environment, making it crucial for realistic rendering.



Materials can look dramatically different depending on the selected HDRI, directly influencing the final appearance of your project. You can find various HDRIs online and easily import them by dragging and dropping the files directly onto the canvas (in `HDR` or `EXR` format).

{% embed url="https://screen.studio/share/I3VsSr7X" %}
Check out how different the materials look with different HDRI
{% endembed %}



{% hint style="info" %}
Environment lighting provided by HDRI can always be supplemented or replaced by **additional light sources** if necessary - [light-sources.md](design-mode/light-sources.md "mention")&#x20;
{% endhint %}

{% hint style="info" %}
To make the HDRI to be visible as a **background**, this can be configured in the background settings - [background.md](background.md "mention")
{% endhint %}



## Settings



Adjusting HDRI settings is essential, as they influence the appearance of materials, reflections, shadows, and even the project size by modifying resolution. Proper attention to these settings is recommended for achieving the best results.

<figure><img src="../../.gitbook/assets/image (401).png" alt="" width="563"><figcaption></figcaption></figure>

* **Intensity** — сontrols the overall brightness of the HDRI environment, affecting how much light is cast onto objects in the scene. The intensity value can be manually set beyond `100` for stronger lighting effects.
* **Rotation** — сhanges the orientation of the HDRI, altering the direction of lighting and reflections.
* **Hue** — adjusts the overall color tint of the HDRI, shifting the color balance of the environment lighting.
* **Saturation** — controls the intensity of colors within the HDRI, allowing for more vivid or muted tones.
* **Shadow** — сontrols the intensity and visibility of shadows cast by the HDRI environment.
* **Blurriness** — softens the HDRI, reducing sharp reflections and creating a more diffused lighting effect. Increasing this setting to the maximum will minimize the visibility of the HDRI in reflections.
* **Resolution** — determines the quality and detail level of the HDRI. Higher resolutions provide sharper reflections but increase project size.



## Library



Read more about this here: [environments-library.md](libraries/environments-library.md "mention")





## Tutorials



{% embed url="https://www.youtube.com/watch?v=Ld9dOsg6cEg" %}





