# Edit mode



## Overview



Edit Mode allows direct manipulation of an object's geometry, enabling **polygonal modeling** by working with vertices, edges, and faces.



### Entering Edit mode

There are three ways to switch to Edit mode:

* Select an object and press **Enter**
* Double-click on an object
* **`Shift+2`**

{% hint style="info" %}
If the object is not a mesh, the system will prompt for confirmation before converting it to mesh geometry
{% endhint %}



### Display and Visibility

* Objects in Edit mode are displayed in [#shaded-display](../control-bar/viewport-display-modes.md#shaded-display "mention")mode by default. This can be overridden using the **`Z`** key to switch display modes.
*   Only one object can be edited at a time. Other objects remain visible in their Design mode appearance or can be displayed as **semi-transparent** by enabling **X-ray Mode** in the menu.<br>

    <figure><img src="../../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>



## Edit Mode Tools



In Edit Mode, tools are specifically designed for working with geometry. Some tools may be inactive if no geometry is selected, as they only apply to specific element types.

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

A dedicated **Control bar** at the bottom of the canvas provides options to switch between editing **vertices** (hotkey - **`1`**)**, edges** (hotkey - **`2`**)**, or faces** (hotkey - **`3`**). In Edit Mode, only one type of geometry can be selected and modified at a time, meaning vertices, edges, and faces cannot be selected or manipulated simultaneously.

<figure><img src="../../../.gitbook/assets/image (87).png" alt="" width="551"><figcaption></figcaption></figure>



<table><thead><tr><th width="192.5703125">Tool</th><th>Description</th></tr></thead><tbody><tr><td><a data-mention href="selection-tools.md">selection-tools.md</a></td><td>A set of tools for selecting vertices, edges, or faces.</td></tr><tr><td><a data-mention href="new-object.md">new-object.md</a></td><td>Create a separate mesh object within the scene.</td></tr><tr><td><a data-mention href="draw.md">draw.md</a></td><td>Manually sketch new geometry.</td></tr><tr><td><a data-mention href="primitives.md">primitives.md</a></td><td>Add basic geometric shapes such as boxes, spheres, and cylinders.</td></tr><tr><td><a data-mention href="extrude.md">extrude.md</a></td><td>Extend geometry outward from a selected face or edge.</td></tr><tr><td><a data-mention href="bevel.md">bevel.md</a></td><td>Smooth sharp edges by adding rounded transitions.</td></tr><tr><td><a data-mention href="make-circle.md">make-circle.md</a></td><td>Transform a selected set of vertices or edges into a circular shape.</td></tr><tr><td><a data-mention href="bridge.md">bridge.md</a></td><td>Connect two separate edge loops with new geometry.</td></tr><tr><td><a data-mention href="slide.md">slide.md</a></td><td>Move edges along their connected geometry.</td></tr><tr><td><a data-mention href="cut.md">cut.md</a></td><td>Create new edges by slicing through geometry.</td></tr><tr><td><a data-mention href="collapse.md">collapse.md</a></td><td>Merge selected vertices, edges, or faces into a single point.</td></tr><tr><td><a data-mention href="cap-open-boundaries.md">cap-open-boundaries.md</a></td><td>Close open areas by generating new faces.</td></tr><tr><td><a data-mention href="merge-faces.md">merge-faces.md</a></td><td>Combine adjacent faces into a single surface.</td></tr><tr><td><a data-mention href="mesh-tools.md">mesh-tools.md</a></td><td>Additional tools for refining and modifying geometry.</td></tr><tr><td><a data-mention href="normals.md">normals.md</a></td><td>Adjust surface normals for proper shading and rendering.</td></tr></tbody></table>







