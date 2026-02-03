# Clipping plane



An invisible plane that clips objects in the scene, useful for sectional views and precise visualization adjustments.

The effect of the clipping plane can be restricted to specific objects, groups, or [selections](../../../other/selections.md).

{% hint style="success" %}
Since the Clipping plane is an object, it can be animated and used in interaction setups
{% endhint %}

{% embed url="https://screen.studio/share/840dQexX" %}

Multiple clipping planes can be used simultaneously, allowing for more complex sectional views and controlled visual effects.



{% hint style="warning" %}
The Clipping plane requires watertight geometry to function correctly. It does not work properly on planes or geometries with open edges.
{% endhint %}



#### Settings



* **Target** — defines an object, group, or [selection](../../../other/selections.md) that the clipping plane will affect.
* **Use material from target** — when disabled, the clipping plane applies its own material. When enabled, it adopts the material of the affected object, ensuring a seamless visual transition.&#x20;



