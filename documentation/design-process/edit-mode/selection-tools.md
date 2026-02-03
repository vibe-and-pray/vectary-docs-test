# Selection tools



## Overview



Selecting geometric elements is one of the most frequent actions when working with geometry. Before using any tool, the necessary geometry must be selected first.

Using **hotkeys** significantly streamlines the selection process, making workflow more efficient.



{% embed url="https://vimeo.com/730330608" %}

In Edit mode, only one type of geometry  - **vertices** (hotkey - **`1)`, edges** (hotkey - **`2`**)**, or faces** (hotkey - **`3`**) - can be selected at a time. After making a selection, the selection mode can be switched. For example, switching from edges to vertices will select all vertices belonging to the previously selected edges.



## Select&#x20;



* The **Select** tool is active by default when no other tool is selected.
* Allows selecting geometry elements one at a time.
* To add elements to the selection, hold **`Shift`** and click on additional elements.
* To remove elements from the selection, hold **`Shift`** and click on an already selected element.
* **Loop selection** allows selecting connected elements in a sequence. Hold **`Alt`** and click on a subsequent element to automatically select all following connected elements. If an element is selected with gaps, the selection pattern will be extended accordingly.



## Marquee



The **Marquee Selection** tool allows selecting multiple geometric elements at once by drawing a selection box over them.

{% hint style="warning" %}
Marquee selection works **through the object**, meaning all geometric elements behind the front-facing ones will also be selected
{% endhint %}

* To **add** elements to the current selection, hold **`Shift`** while making a new selection.
* To **remove** elements from the selection, hold **`Alt`** while selecting.
* Pressing the **`M`** key repeatedly cycles through different selection modes, allowing for quick switching between selection methods.



## Lasso



The **Lasso Selection** tool allows freeform selection of geometric elements by drawing a custom shape around them. The selection does not require closing the shape manually - simply releasing the mouse button will complete the selection automatically.

{% hint style="warning" %}
Lasso selection works **through the object**, meaning all geometric elements behind the front-facing ones will also be selected
{% endhint %}

* Hold **Shift** while selecting to **add** elements to the current selection.
* Hold **Alt** while selecting to **remove** elements from the selection.
* Pressing the **`L`** key repeatedly cycles through different selection modes, allowing for quick switching between selection methods.



## Paint Select



The **Paint Selection** tool allows selecting multiple geometric elements by brushing over them with a cursor.

* Hold **Shift** while painting to **add** elements to the selection.
* Hold **Alt** while painting to **remove** elements from the selection.
* Pressing the **`P`** key repeatedly cycles through different selection modes, allowing for quick switching between selection methods.



## Select All



The **Select All** function allows quick selection of connected or entire geometry within an object.<br>

* Press **Ctrl + A** to select all connected geometry related to the initially selected element.
* Press **Ctrl + A** again to expand the selection to the entire object.



## Invert Selection



The **Invert Selection** function allows quickly selecting all unselected elements while deselecting the currently selected ones.





## Selection jog



The **Selection Jog** tool provides access to various selection methods, adapting to the type of geometric element selected before activation. It can be quickly accessed using the **`K`** hotkey.

<figure><img src="../../../.gitbook/assets/image (249).png" alt="" width="242"><figcaption></figcaption></figure>

{% embed url="https://vimeo.com/731009919" %}

* **Loop Selection** – selects a continuous edge loop
* **Lines by Angle** – selects connected edges based on a specified angle threshold
* **Select Planar** – selects faces that are part of the same plane
* **Invert Selection** – inverts the current selection, selecting unselected elements and deselecting the current ones
* **Select Similar** – selects elements similar to the currently selected one based on shared properties
* **Select Holes** – identifies and selects holes in the mesh
* **Select Polygon** – selects polygons with a specific number of edges
* **Grow / Shrink** – expands or contracts the current selection incrementally



