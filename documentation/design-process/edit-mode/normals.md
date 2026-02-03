# Normals

Normals define the direction in which a surface faces, affecting shading, lighting, and rendering. By default, normals are rendered on one side of a face unless the **double-sided material** option is enabled. Properly configured normals help ensure accurate light reflections and prevent visual artifacts in rendering.

The **Normals** toolset provides options for adjusting the direction and smoothness of surface shading in a mesh.<br>

* **Flip Normals** — Reverses the direction of selected faces' normals. Useful for correcting incorrect shading or fixing inward-facing geometry.
* **Unify Normals** — Aligns all selected normals to face the same direction. Helps resolve inconsistencies in surface orientation for uniform shading.
* **Smooth Threshold** — Controls the angle at which normals are blended for smooth shading. Lower values maintain hard edges, while higher values create a smoother appearance between connected faces.

{% embed url="https://vimeo.com/736558289" %}
