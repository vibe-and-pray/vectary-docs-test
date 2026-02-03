# Modifiers



## Overview



Modifiers are tools used to procedurally alter the geometry of objects in a non-destructive manner. They allow for dynamic adjustments and efficient modeling workflows by applying transformations, duplications, and shape modifications without permanently affecting the base mesh. Modifiers can be stacked and combined to achieve complex designs while maintaining flexibility for future edits.



<div align="left"><figure><img src="../../../../.gitbook/assets/image (294).png" alt="" width="375"><figcaption></figcaption></figure></div>



A modifier functions as a group, meaning it can be applied to multiple objects simultaneously. Additionally, one modifier can be applied to another, allowing for complex, layered transformations.&#x20;

<div align="left"><figure><img src="../../../../.gitbook/assets/image (108).png" alt="" width="247"><figcaption></figcaption></figure></div>



The effect of a modifier can be temporarily disabled without removing it, providing flexibility in testing different configurations:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (296).png" alt="" width="262"><figcaption></figcaption></figure></div>



To remove a modifier without deleting its contents, open the context menu and select **Ungroup** **`Ctrl+Shift+G`**

<div align="left"><figure><img src="../../../../.gitbook/assets/image (297).png" alt="" width="363"><figcaption></figcaption></figure></div>



## Converting to geometry



Any modifier can be converted into geometry, preventing the system from recalculating operations each time, which improves performance while working in Studio.&#x20;

This is especially recommended for modifiers such as **Subdivide**, **Boolean**, and **Bevel**.

Converting **Array** and **Symmetry** modifiers into geometry will result in instances rather than independent objects. The geometry of these instances remains linked, meaning they do not increase the overall polygon count while still behaving as duplicated elements of the original object.

{% hint style="info" %}
Conversion is relevant only for Studio and does not affect the web viewer
{% endhint %}

<div align="left"><figure><img src="../../../../.gitbook/assets/image (106).png" alt="" width="375"><figcaption></figcaption></figure></div>



## List of modifiers



<table><thead><tr><th width="146.15234375">Type</th><th>Description</th></tr></thead><tbody><tr><td><a data-mention href="array-linear.md">array-linear.md</a></td><td>Creates multiple instances of an object along a straight line with adjustable spacing and count parameters.</td></tr><tr><td><a data-mention href="array-radial.md">array-radial.md</a></td><td>Duplicates an object around a central point, allowing control over the number of copies, rotation, and distribution radius.</td></tr><tr><td><a data-mention href="array-grid.md">array-grid.md</a></td><td>Generates a grid-based duplication pattern with customizable rows, columns, and depth settings.</td></tr><tr><td><a data-mention href="array-object.md">array-object.md</a></td><td>Uses another object as a reference to distribute instances along its surface.</td></tr><tr><td><a data-mention href="subdivide.md">subdivide.md</a></td><td>Divides the geometry into smaller segments, increasing mesh density for smoother deformations.</td></tr><tr><td><a data-mention href="../../edit-mode/bevel.md">bevel.md</a></td><td>Adds chamfered edges to a model by smoothing sharp corners and refining geometry.</td></tr><tr><td><a data-mention href="randomize.md">randomize.md</a></td><td>Applies random transformations to objects, including position, rotation, and scale, for more organic variations.</td></tr><tr><td><a data-mention href="symmetry.md">symmetry.md</a></td><td>Mirrors an object along a chosen axis, ensuring that modifications on one side are automatically reflected on the other.</td></tr><tr><td><a data-mention href="boolean.md">boolean.md</a></td><td>Performs operations between two objects, such as union, subtraction, and intersection, to create complex shapes.</td></tr></tbody></table>





