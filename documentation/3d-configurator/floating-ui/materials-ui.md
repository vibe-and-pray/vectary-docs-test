# Materials (UI)

The **Materials** UI element enables end users to switch between different materials assigned to an object. It can be displayed as either a **dropdown menu** or a **swatch selection**.



* To enable material switching, multiple materials must first be assigned to an object. When this object is set as the **source** for the **Materials UI element**, the element dynamically displays all available materials. \
  **Learn more** about adding materials: [#how-to-add-a-material](../../design-process/materials-and-textures/#how-to-add-a-material "mention")
* Material switching can also be configured using the [Materials action](../interactions/actions/materials.md).&#x20;



#### Settings



* **Source** — select the object whose materials will be controlled.
* **Style** — choose the switcher style: **Swatch** or **Dropdown**.

{% hint style="info" %}
If the [variants.md](../variants.md "mention") is selected as the **Source**, the **Materials** element will display materials of the currently active object within the **Variants** group.
{% endhint %}

{% hint style="success" %}
The **Swatch** style allows custom thumbnails to be uploaded for each material.
{% endhint %}



* **Auto-hide** — Hides the UI element when the object is hidden.
* **Include hidden objects** — If enabled, material switching will also affect hidden objects.



**Additional settings for Swatch style:**



* **Display name** — Show the selected material name and display it on hover over the thumbnail.
* **Alignment** — Set thumbnail alignment.
* **Spacing** — Define the spacing between thumbnails.
* **Swatch size** — Set the thumbnail size.



#### Layout



* **W** — Defines the width of the **Materials** element.
* **H** — Defines the height of the **Materials** element.<br>
* **Fixed** — Sets a fixed size in pixels.
* **Fill** — Adjusts the size based on the parent element (**Floating UI** or **Container**).<br>
* **Padding** — Sets vertical and horizontal padding within the element.
* **Corner radius** — Defines the rounding radius for thumbnails (**Swatch** style) or the dropdown field (**Dropdown** style).



#### Stroke



* **Thickness** — Defines the stroke thickness for the thumbnails or dropdown field.
* **Default color** — Sets the default stroke color (if disabled, the stroke will be transparent).
* **Hover color** — Changes the stroke color on hover.
* **Active color** — Defines the stroke color of the selected material thumbnail.





