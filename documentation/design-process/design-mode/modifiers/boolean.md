# Boolean



## Overview



Boolean modifier performs operations between multiple objects to create complex shapes. The bottom object in the list acts as the main object, while all other objects above it participate in the operation with the main object.

<figure><img src="../../../../.gitbook/assets/image (382).png" alt="" width="563"><figcaption></figcaption></figure>



Each participating object has an icon next to it that determines which of the three operations will be performed: **union**, **subtract**, or **intersect**. This means that the main object can have different types of operations with different objects simultaneously.

<figure><img src="../../../../.gitbook/assets/image (383).png" alt="" width="366"><figcaption><p>to change the operation type, click on the icon</p></figcaption></figure>



{% hint style="success" %}
The main object can be changed at any time by dragging another object to the bottom of the list
{% endhint %}



### **Separate by material**



Enabling this option ensures that each object involved in the Boolean operation retains its original material.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (334).png" alt="" width="244"><figcaption></figcaption></figure></div>

{% hint style="info" %}
When this option is enabled, converting to geometry preserves the number of objects involved in the operation. If disabled, the conversion results in a single object.
{% endhint %}





### Boolean Animation Limitations



{% hint style="warning" %}
#### Limitation



* Animation and transformation of **objects** under a Boolean modifier are visible only in the Shared version of the project. In the Preview version, this does not work.<br>
* Animation of **Boolean operations** is not supported. It works in the Preview version but is not functional in the Shared version.
{% endhint %}







## Union



Merges objects into a single shape while ensuring that the resulting geometry remains correct.

{% embed url="https://vimeo.com/741459725" %}

Unlike a simple merge operation, this method removes internal geometry at intersections, preventing unnecessary overlapping polygons.

<figure><img src="../../../../.gitbook/assets/image (335).png" alt="" width="563"><figcaption></figcaption></figure>



## Subtract



Cuts the participating objects from the main object, removing overlapping sections and leaving behind the remaining shape.

{% embed url="https://vimeo.com/741445919" %}



## Intersect



Keeps only the overlapping parts between the main object and participating objects, removing all non-overlapping sections.

{% embed url="https://vimeo.com/741459702" %}





## Tutorial



{% embed url="https://youtu.be/I_MhWLuDCmM" %}



