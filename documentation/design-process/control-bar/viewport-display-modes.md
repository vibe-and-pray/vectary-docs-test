# Viewport display modes



### Overview



Viewport display modes control how objects appear in the scene, allowing adjustments to visibility to provide additional visual information while working on a project.

By default, in **Design mode**, objects are displayed with their assigned materials and textures

To view an object's mesh or change its appearance, switch the display mode from the list or cycle through the modes by pressing **`Z`**.

<figure><img src="../../../.gitbook/assets/image (92).png" alt="" width="507"><figcaption></figcaption></figure>

{% hint style="success" %}
Display modes can be applied globally or to individual objects:

* If an object is selected, the display mode change applies only to that object
* If no objects are selected, the change affects all objects in the scene
{% endhint %}





### Lightmap preview



Used to preview how an object will look with a baked Lightmap. This helps assess different lighting conditions before finalizing baking, saving time on multiple iterations.

This mode does not use real-time rendering but relies on **path tracing**, making it more resource-intensive and introducing noise (there is no denoiser option available for this mode).



### Textured display **(Default)**



Displays objects with their assigned materials, including textures, shadows, reflections, and lighting.



### Shaded display&#x20;



Applies a uniform shading style to objects, filling them with a gradient color while preserving shading. This mode is useful for reviewing scene composition and object placement.

* Wireframe meshes are visible, making it easier to analyze and optimize complex models
* Used in [edit-mode](../edit-mode/ "mention") for clearer mesh adjustments



### **Wireframe display**



Shows objects as transparent wireframe outlines

* Helps identify objects with complex meshes, allowing performance optimization.
* Useful in **Edit Mode**, as it eliminates the need to rotate the camera to see through objects.



## Bounding box display



Simplifies scene navigation by displaying objects as bounding boxes, showing only the space they occupy without detailed meshes.

* Useful for working with large, complex scenes where performance is a concern.

