# Gizmo & Origin



## Overview



The **Gizmo** and **Origin** (pivot point) are essential tools for manipulating objects in the 3D scene. They control how objects are positioned, rotated, and scaled, ensuring precise transformations and alignment.\
\
Understanding and adjusting the Gizmo and Origin allows for greater precision when working with 3D models, ensuring efficient object manipulation and alignment.



<figure><img src="../../../.gitbook/assets/image (411).png" alt="" width="467"><figcaption></figcaption></figure>



## Gizmo



The **Gizmo** is an interactive tool used for transforming objects in the viewport. It provides handles for moving, rotating, and scaling objects along specific axes.



The **Gizmo** can operate in two modes: **Global** and **Local**. The axes of the **Global Gizmo** align with the scene’s world axes, while the **Local Gizmo** aligns with the object's own orientation. Switching between these modes is done using the hotkey **`W`**.

<figure><img src="../../../.gitbook/assets/Clipboard-20250311-125109-155.gif" alt="" width="498"><figcaption></figcaption></figure>



The **Advanced Gizmo** option adds additional controls, allowing transformations along two axes simultaneously.

<figure><img src="../../../.gitbook/assets/image (417).png" alt="" width="375"><figcaption></figcaption></figure>



### Position



* To move an object, <mark style="color:yellow;">**left-click**</mark> and drag a Gizmo arrow
* To move the Gizmo itself without affecting the object, <mark style="color:red;">**right-click**</mark> and drag an arrow

<figure><img src="../../../.gitbook/assets/image (415).png" alt="" width="563"><figcaption></figcaption></figure>

* Clicking on an arrow opens a field to enter an exact movement value:

<figure><img src="../../../.gitbook/assets/image (416).png" alt="" width="517"><figcaption></figcaption></figure>



### **Scaling**



* To scale an object, use the small cubes on the Gizmo guides
* To scale along a single axis, hold **`Shift`**, then drag the cube of the desired axis
* Clicking on a cube opens a field to enter an exact scaling value

<figure><img src="../../../.gitbook/assets/image (418).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
Transformations occur relative to the **Origin**
{% endhint %}



After scaling, it is recommended to apply the scale so that all axes equal 1, preventing potential issues:&#x20;

<figure><img src="../../../.gitbook/assets/image (419).png" alt="" width="356"><figcaption></figcaption></figure>



### **Rotation**



* To rotate an object, <mark style="color:yellow;">**left-click**</mark> and drag one of the Gizmo arcs
* To rotate the Gizmo itself without affecting the object, <mark style="color:red;">**right-click**</mark> and drag an arc
* Holding **`Shift`** enables 15-degree incremental rotation
* Clicking on an arc opens a field to enter an exact rotation value

<figure><img src="../../../.gitbook/assets/image (420).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
Rotation occurs relative to the **Origin**
{% endhint %}

{% hint style="info" %}
The rotation angle increment depends on [angle snapping](snapping.md#angle) (if active)
{% endhint %}





## Origin (pivot point)



The Origin (pivot point) serves as the anchor for all transformations, including movement, rotation, scaling, and snapping. Its position determines how an object interacts with transformations, influencing the way it moves, rotates, and scales within the scene.

<figure><img src="../../../.gitbook/assets/image (421).png" alt="" width="563"><figcaption></figcaption></figure>



**Repositioning the Origin** – the origin can be moved independently or along with the object:

* <mark style="color:yellow;">**Left-click**</mark>**&#x20;and drag** to move the origin together with the object
* <mark style="color:red;">**Right-click**</mark>**&#x20;and drag** to move the origin without affecting the object's position



#### **Aligning the Origin to Key Points**

To snap the origin to the **lowest**, **middle**, or **top** point of the object, <mark style="color:red;">**right-click**</mark> the origin. Snap points will appear along the <mark style="color:blue;">**Z-axis**</mark>, allowing for quick repositioning. To adjust along a different plane, change the axis orientation.

<figure><img src="../../../.gitbook/assets/image (422).png" alt="" width="563"><figcaption></figcaption></figure>



{% hint style="success" %}
**Resetting the Origin** – Double-clicking the origin automatically moves it to the lowest part of the object
{% endhint %}



Snapping to the _Grid_ or _Face_ applies specifically to the Origin and occurs perpendicular to the <mark style="color:blue;">**Z-axis**</mark>.\
Read more: [snapping.md](snapping.md "mention")

<figure><img src="../../../.gitbook/assets/image (423).png" alt="" width="446"><figcaption></figcaption></figure>



## Tutorials



{% embed url="https://www.youtube.com/watch?v=cOXbik0CWhw" %}





