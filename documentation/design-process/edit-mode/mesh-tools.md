# Mesh Tools

The **Mesh Tools** set provides various operations for refining and modifying geometry, ensuring better topology and surface control.

Press **`J`** to activate the Mesh Tools menu.

<figure><img src="../../../.gitbook/assets/image (252).png" alt="" width="312"><figcaption></figcaption></figure>

Weld — merges overlapping or nearby vertices into a single point. When used on disconnected geometry, it helps unify separate elements into a single structure.

{% embed url="https://screen.studio/share/hsz6KS4Y" %}

* **Smooth** – Softens the mesh by averaging vertex positions, reducing sharp edges and irregularities.
* **Triangulate** – Converts all faces into triangles, useful for exporting to certain rendering engines and game engines.
* **Quadify** – Converts triangulated or irregular geometry into quads, improving topology for subdivision modeling.
* **Spherify** – Adjusts the shape of the selected geometry to approximate a sphere while maintaining the original vertex count.
* **Subdivision** – Increases mesh resolution by adding additional geometry for smoother surfaces.
* **Flat Subdivision** – Subdivides without smoothing, preserving the original shape while adding more detail.
* **Interpolated Subdivision** – Creates smooth interpolated subdivisions, balancing shape retention and curvature.
* **Approximated Subdivision** – Applies a more flexible subdivision method, approximating the shape rather than strictly interpolating.
* **Approximated Desubdivision** – Attempts to revert a subdivided mesh to a lower-resolution form while maintaining its overall structure.

