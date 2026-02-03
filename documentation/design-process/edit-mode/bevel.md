# Bevel

The **Bevel** tool modifies mesh geometry by adding extra geometry along selected edges, vertices, or faces. Beveling edges creates smooth transitions between surfaces, beveling vertices results in a rounded corner effect, and beveling faces offsets the selection inward, generating additional geometry around the perimeter.

{% hint style="info" %}
Bevel tool can be applied to multiple geometric elements at once
{% endhint %}

{% embed url="https://vimeo.com/733555959" %}

#### How it works

* Select an edge, vertex, or face before activating the tool
* Press **`B`** to activate Bevel mode
* After activating Bevel mode, a blue handle appears.
  * dragging the handle adjusts the bevel offset, generating new geometry based on the selected elements.
  * clicking on the handle opens a context menu with additional options such as segment count, offset, and other settings for precise control.



#### Context menu options



* **Offset** – Adjusts the distance by which the beveled edge or vertex is pushed outward from its original position.
* **Inset** – Offsets the beveled face inward, adjusting the distance from its original position.
* **Limits** – Restricts the bevel's expansion, preventing it from extending beyond intersecting edges.
* **Segments** – Defines the number of subdivisions along the bevel, increasing smoothness by adding more geometry.
* **Separate Faces (Off)** – Bevels each selected face independently, without merging adjacent beveled faces.
* **Group Faces (On)** – Treats all selected faces as a single surface, ensuring a continuous bevel across them.
* **Sharp Segments** – Adds additional geometry without rounding, maintaining sharp edges while increasing detail.
* **Round Segments** – Generates a smooth, curved bevel by distributing segments evenly along the rounded surface (default setting).



