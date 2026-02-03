# Visibility

The **Visibility** action allows controlling the visibility of any object in the scene, including **Floating UI** elements.

<figure><img src="../../../../.gitbook/assets/image (235).png" alt="" width="563"><figcaption></figcaption></figure>

**Settings**<br>

* **Control:**
  * **Toggle** — Switches visibility on or off.
  * **Show** — Makes the object visible.
  * **Hide** — Hides the object.

{% tabs %}
{% tab title="Object" %}
Choose object.
{% endtab %}

{% tab title="Selection" %}
Choose [selection](../../../other/selections.md).
{% endtab %}

{% tab title="Floating UI" %}
* **Parent** — Select the [floating-ui](../../floating-ui/ "mention")
* **Target** — Choose the specific **Floating UI** element to be controlled (_image_, _button_, etc.)
* **Relative to** — Defines the reference point for the element’s position:
  * **Self** — Appears relative to the object defined in the trigger.
  * **Canvas** — Appears relative to the canvas.
  * **Pointer** — Appears relative to the cursor.

> **Note:** To adjust the angle and offset of the element, configure the **Position and Offset** parameters in the **Floating UI** settings within Design mode.

* **Auto-hide** — Automatically hides the element when clicking anywhere outside of it.
{% endtab %}
{% endtabs %}



