# Materials



Materials can impact both project size and rendering performance, especially when using advanced visual effects.&#x20;

Here are some tips and recommendations to help optimize material usage:



* **Remove unused materials** – if you've experimented with materials during scene creation, some objects may have multiple materials assigned. Remove any unused or unnecessary materials to reduce project size.

<div align="left"><figure><img src="../../../.gitbook/assets/image (59).png" alt="" width="279"><figcaption></figcaption></figure></div>



*   **Optimize Opacity usage**\
    <br>

    * When using [**Opacity**](../../design-process/materials-and-textures/basic-materials/opacity.md), prefer the **Mask** method whenever possible. It has minimal performance impact and can often deliver better visual results.\
      <br>
    * The **Blend** method can significantly affect performance, especially when transparent objects are placed in front of other geometry.\
      <br>
    * Avoid covering large areas of the screen with **Blend**-based opacity to maintain smooth rendering.<br>

    <div align="left"><figure><img src="../../../.gitbook/assets/image (60).png" alt="" width="375"><figcaption><p><br><br></p></figcaption></figure></div>


* **Use** [**Subsurface**](../../design-process/materials-and-textures/advanced-materials/subsurface.md) **cautiously** – this property has a medium impact on performance. Try not to apply it to materials that occupy most of the screen.\
  <br>
* **Refraction usage** – [Refraction](../../design-process/materials-and-textures/advanced-materials/refraction.md) can be very demanding. If used on large objects or elements that take up a lot of screen space, it can dramatically reduce performance. Use sparingly.\
  <br>
* **Clearcoat** – in certain cases, [Clearcoat](../../design-process/materials-and-textures/advanced-materials/clearcoat.md) may have a moderate effect on performance. Avoid using it extensively across the scene, especially on full-screen elements.





