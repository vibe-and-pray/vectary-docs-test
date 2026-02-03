# Selections



## Overview



Selection is a virtual group of multiple objects that are independent of the object list structure. This allows multiple objects from different groups to be combined without changing the project structure. The resulting selection can then be specified in the settings of various tools and features.

<figure><img src="../../.gitbook/assets/image (523).png" alt=""><figcaption></figcaption></figure>



## How to open Selection Manager



{% tabs %}
{% tab title="Method 1" %}
**Selection Manager** can be accessed from the [selection tools](../design-process/design-mode/selections-tools.md) panel.

<div align="left"><figure><img src="../../.gitbook/assets/image (522).png" alt="" width="237"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Method 2" %}
**Selection Manager** can also be opened from the [Interactions](../3d-configurator/interactions/) settings tab, under the `Selection` section.

<div align="left"><figure><img src="../../.gitbook/assets/image (524).png" alt="" width="563"><figcaption></figcaption></figure></div>
{% endtab %}
{% endtabs %}





## How to create a new Selection



{% tabs %}
{% tab title="Method 1" %}
Select the required objects either in the left panel or directly on the canvas. Then, right-click to open the context menu and choose **`Create new selection`**.

<div align="left"><figure><img src="../../.gitbook/assets/image (525).png" alt="" width="375"><figcaption></figcaption></figure></div>
{% endtab %}

{% tab title="Method 2" %}
If the **Selection Manager** is open, clicking **`+ Selection`** will create a new selection from the currently selected objects.

<div align="left"><figure><img src="../../.gitbook/assets/image (526).png" alt="" width="563"><figcaption></figcaption></figure></div>
{% endtab %}
{% endtabs %}



## Editing an existing Selection



Click an existing selection in the Selection Manager to display its objects in the right panel.

<img src="../../.gitbook/assets/image (528).png" alt="" data-size="line">   - **plus icon (+)** adds new objects to a Selection. First, select objects to be added, then click the icon.

<img src="../../.gitbook/assets/image (530).png" alt="" data-size="line">  - **minus icon (–)** removes objects from a Selection.

<img src="../../.gitbook/assets/image (533).png" alt="" data-size="line">  - **target icon** selects all objects included in a Selection

<figure><img src="../../.gitbook/assets/image (527).png" alt=""><figcaption></figcaption></figure>





## Where Selections can be used



* [**Floating UI – Materials**](../3d-configurator/floating-ui/materials-ui.md)**:** when a selection is defined as the source, material switches affect all objects within that selection.
* [**Augmented Reality – Limit objects**](../project-settings/augmented-reality-webar.md)**:** specifies which objects should be displayed in AR mode.
* [**Reflections – Limit objects**](../design-process/effects/reflections.md)**:** defines which objects will have reflections enabled.
* [**Interactions**](../3d-configurator/interactions/) **settings:** in some interactions, both individual objects and entire selections can be used as targets.



{% hint style="info" %}
The list of Studio features supporting selections is continuously expanding.
{% endhint %}



## Selection Manager and Selections — Tips



* Hovering over a selection in the Selection Manager temporarily hides all other objects in the scene, helping to visualize which objects are included.

{% embed url="https://screen.studio/share/DrIWYbiW" %}



* A new project can be created from a selection by selecting multiple objects, right-clicking, and choosing **`Create project from selection`**.\
  \
  ![](<../../.gitbook/assets/image (535).png>)



* Selection Manager window can be resized and repositioned.\
  \
  <img src="../../.gitbook/assets/Clipboard-20251030-142644-536.gif" alt="" data-size="original">\
  <br>







