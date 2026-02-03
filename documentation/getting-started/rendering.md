---
description: WYSIWYG - What You See Is What You Get
---

# Rendering



Vectary utilizes **real-time**, **photorealistic** rendering, which is **always active** and cannot be disabled.

To ensure optimal performance, certain [effects](../design-process/effects/) require manual activation when needed:, to maintain good performance, some effects need to be enabled manually when necessary:

* [Reflections](../design-process/effects/reflections.md)
* [Soft shadows](../design-process/effects/soft-shadows.md)
* [Ambient occlusion](../design-process/materials-and-textures/baked-textures/ambient-occlusion-texture.md)
* [Bloom](../design-process/effects/bloom.md)

[Lighting](../design-process/environment.md) plays a crucial role in defining material appearance. With a well-configured lighting setup, materials within the scene can achieve a more refined and realistic look, especially when using [advanced materials](../design-process/materials-and-textures/advanced-materials/) (refraction, subsurface scattering, etc.).



For high-resolution render exports, use the button located at the bottom of the canvas.

<figure><img src="../../.gitbook/assets/image (118).png" alt="" width="563"><figcaption></figcaption></figure>



<details>

<summary>Photon and Instant render <strong>(legacy)</strong></summary>

The menu includes two legacy renderers — Instant and Photon — retained from the previous version for users who may still need them. However, there are important considerations:

* **Instant** — no longer functional, but still allows exporting images at the desired resolution.
* **Photon** — remains operational but is no longer supported, which may result in occasional bugs.

While Photon has delivered impressive results, the era of real-time rendering has arrived. The new real-time rendering engine already achieves results comparable to Photon and, in some cases, matches its quality entirely. In specific scenarios, Photon may still outperform, but continuous improvements are being made to optimize real-time rendering quality.

Real-time rendering in Vectary captures every step of the creative process as it happens, reflecting changes and edits instantly. This immediate feedback is essential for efficient design workflows, eliminating the need to wait for renders during 3D content creation.

</details>





