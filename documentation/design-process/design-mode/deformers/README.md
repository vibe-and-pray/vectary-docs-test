# Deformers



## Overview



Deformers are procedural tools used to modify the shape of objects without altering their underlying topology. They allow for flexible transformations that can be adjusted dynamically

<figure><img src="../../../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (107).png" alt="" width="375"><figcaption></figcaption></figure></div>



A deformer functions as a group, meaning it can be applied to multiple objects simultaneously. Additionally, one deformer can be applied to another, allowing for complex, layered transformations.&#x20;

<div align="left"><figure><img src="../../../../.gitbook/assets/image (109).png" alt="" width="239"><figcaption></figcaption></figure></div>



The effect of a deformer can be temporarily disabled without removing it, providing flexibility in testing different configurations:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (110).png" alt="" width="398"><figcaption></figcaption></figure></div>



To remove a modifier without deleting its contents, open the context menu and select **Ungroup** **`Ctrl+Shift+G`**

<div align="left"><figure><img src="../../../../.gitbook/assets/image (111).png" alt="" width="346"><figcaption></figcaption></figure></div>



## Edit mode



The deformer’s area of effect can be adjusted in Edit mode. To enter this mode, select the deformer and click the Edit button. \
While in Edit mode, the shape of the area of effect can be modified using the gizmo by moving or scaling it.\
Additionally, the Type setting (Unlimited, Limited, Within Box), found among other deformer settings, influences the deformer’s area of effect.





## Converting to geometry



Any deformer can be converted into geometry, preventing the system from recalculating operations each time, which improves performance while working in Studio. This is particularly important for the **Simplify** deformer, as its calculations require significant resources.&#x20;

{% hint style="info" %}
Conversion is relevant only for Studio and does not affect the web viewer
{% endhint %}

<div align="left"><figure><img src="../../../../.gitbook/assets/image (112).png" alt="" width="311"><figcaption></figcaption></figure></div>



## List of deformers



<table><thead><tr><th width="134.7890625">Type</th><th>Description</th></tr></thead><tbody><tr><td><a data-mention href="bend.md">bend.md</a></td><td>Applies a curvature to an object, bending it along a defined axis. </td></tr><tr><td><a data-mention href="twist.md">twist.md</a></td><td>Rotates an object around its axis, creating a spiral effect. </td></tr><tr><td><a data-mention href="taper.md">taper.md</a></td><td>Gradually scales an object along a chosen axis, making one end narrower or wider than the other.</td></tr><tr><td><a data-mention href="skew.md">skew.md</a></td><td>Shears an object along an axis, shifting its top or bottom relative to the base, creating a slanted appearance.</td></tr><tr><td><a data-mention href="stretch.md">stretch.md</a></td><td>Scales an object along a single axis while maintaining its proportions on other axes, elongating or compressing the shape.</td></tr><tr><td><a data-mention href="spherify.md">spherify.md</a></td><td>Transforms an object’s shape towards a perfect sphere, adjusting its form while preserving the original volume.</td></tr><tr><td><a data-mention href="noise.md">noise.md</a></td><td>Applies randomized displacement to an object's surface, creating an organic, irregular look.</td></tr><tr><td><a data-mention href="simplify.md">simplify.md</a></td><td>Reduces the complexity of an object's geometry, optimizing its topology while maintaining overall shape integrity.</td></tr></tbody></table>









