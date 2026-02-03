# Geometry



Geometry - meaning the number of objects and polygons in a scene - is one of the main factors affecting both project size and real-time performance.

Reducing polygon count wherever possible is always a good practice. While scenes with up to **500,000 polygons** generally perform well, performance may degrade beyond that. The recommended target is **under 100,000 polygons** for the best experience.&#x20;

For **AR projects**, keeping polygon count below **100,000** is recommended.



#### Tips for reducing geometry



1. **Simplify modifier** – use the [Simplify modifier](../../design-process/design-mode/deformers/simplify.md) to reduce polygon count while maintaining the overall shape of the object. Note that very high-polygon models may cause the browser tab to become unresponsive.\
   <br>
2. **Use linked duplicates (instances)** – for repeating objects, use **linked duplicates** instead of full copies. Use **`Ctrl+Shift+D`** or the right-click context menu to create an instance. Instances share geometry, meaning they do not increase polygon count. Changes made to one instance update all linked ones. This same principle applies to [Array modifiers](../../design-process/design-mode/modifiers/#list-of-modifiers).\
   <br>
3. **Simplify distant or hidden objects** – for objects that are far away or barely visible in the scene, consider reducing their detail or simplifying their geometry.\
   <br>
4. **Remove internal or hidden geometry** – some models may contain internal geometry or objects that are not visible. These should be removed or hidden to reduce complexity.\
   <br>
5. **Weld disconnected parts** – in geometry [Edit mode](../../design-process/edit-mode/), use the [Weld tool](../../design-process/edit-mode/mesh-tools.md) to merge disconnected parts into a single mesh. This helps simplify and optimize the model.  &#x20;



