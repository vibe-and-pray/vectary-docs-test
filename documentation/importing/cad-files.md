---
description: Turn your CAD models into interactive experiences
---

# CAD files



## Overview



Vectary supports **`STEP`**/**`STP`** , **`IGES`**/**`IGS`** formats, which are mainly used in the CAD workflow. Once such a file is imported, its structure is converted into one or multiple **`NURBS`** objects.



A **`NURBS`** is a special object that contains **`NURBS`** geometry. Since Vectary is a mesh software, the imported **`NURBS`** geometry is automatically converted into mesh geometry. However, this transformation is procedural, which means that the quality can be changed at any time (similar to segment parameters for primitive objects).





## What are the benefits of the CAD importer?

* Using additional software to convert CAD files into Vectary is unnecessary. Simply drag and drop your created or downloaded file.
* The quality of any part of the object can be adjusted, helping achieve a balance between polygon count and model detail. The benefit of keeping the **`NURBS`** object is that there is no need to create a new model, just to change settings.
* Better suited for companies using CAD file workflow.
* **`STEP`**/**`STP`** , **`IGES`**/**`IGS`** are files that allow you to export only the data you need, not the entire project.



## Import



Importing can take some time (a few minutes in some circumstances).

{% embed url="https://screen.studio/share/A38Spo3h" %}



*   When importing a file, the parameters of all objects are adjusted relative to the size of the largest object in the file.

    _Import example:_

    1. Small screw - high quality of detail.
    2. A whole CNC machine with many small parts - the quality of small parts will be low to avoid many polygons.
* We recommend the size of the **`STEP`**/**`IGES`** file up to 50MB. Files exceeding this size may be processed for too long. If the file exceeds the mentioned size, it is best practice to export in standard OBJ format, import to Vectary, and use the Simplify plugin to decrease the polygon density.
* Vectary only supports geometry that can be directly converted to polygons, meaning we do not support **curves** or **points**. We only support surfaces and polyfaces.



{% hint style="info" %}
Vectary offers the ability to import CAD files, which can be a valuable feature. However, it is important to note that there are some limitations.



In most cases, we recommend importing files as mesh geometry (such as **`OBJ`**, **`FBX`**, **`GLTF`**, **`GLB`**, or **`STL`**). This is because **`STEP`** and **IGES** are old formats and there may be differences in the way each software interprets these formats, namely different object structure, geometry, and materials.
{% endhint %}





## File structure



Notice that NURBS objects have the following icons in the left panel:

<div align="left"><figure><img src="../../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure></div>

Imported NURBS geometry can contain multiple parts. in that case, it is imported as multiple NURBS objects under the group (the name of the group is the name of the file).

<div align="left"><figure><img src="../../.gitbook/assets/image (326).png" alt="" width="372"><figcaption></figcaption></figure></div>

In some cases, there is the button Break apart which will change the current object to multiple parts:

{% embed url="https://screen.studio/share/B6sWbmLy" %}



## Meshing management



The settings allowing for changes in the density and quality of the mesh are located on the right panel.



<div align="left"><figure><img src="../../.gitbook/assets/image (327).png" alt=""><figcaption><p>Default settings</p></figcaption></figure></div>



{% hint style="info" %}
These parameters can be adjusted either for an individual object or for all selected objects
{% endhint %}

{% hint style="info" %}
It is not necessary to modify all of the values at once; instead, try to change each one a little at a time
{% endhint %}



Default values may result in distorted geometry. However, you can define the level of detail for each part of the object yourself. It is important to note that increasing the level of detail leads to an increase in the number of polygons, which results in a larger file size and can potentially affect the performance of the project.



<figure><img src="../../.gitbook/assets/image (328).png" alt=""><figcaption><p>Geometry distortion example</p></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (329).png" alt=""><figcaption><p>After changing the quality settings</p></figcaption></figure>



**Linear deflection** - defines the maximum distance between the original NURBS geometry and final mesh geometry (strong impact on the polygon count).

**Angular deflection** - defines the maximum angle between 2 polygons (minimal impact on the polygon count).

**Min edge size** - defines the minimum length of the edge (average impact on the polygon count).



<figure><img src="../../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
The lower the number, the more precise the result is, but number of polygons also increases
{% endhint %}



After changing the parameters in the upper right corner of the scene you can see the status of the recalculation:

<figure><img src="../../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure>



## Converting to geometry



The imported CAD file becomes a NURBS object, which in turn is a procedural object whose quality parameters can be changed at any time.

If it is necessary to edit the mesh, the object must be converted to a geometric one. At the same time you lose the ability to adjust the quality (works similarly to primitives).



<figure><img src="../../.gitbook/assets/34treg.gif" alt=""><figcaption><p>Note the different icons for a NURBS object and a geometric one</p></figcaption></figure>



Each change in quality settings is based on the original file, so you can safely experiment with the settings.





## Tutorials



{% embed url="https://youtu.be/t_0uFBkQCdI?si=W4-ySJpjHEaj3HJL" %}

{% embed url="https://youtu.be/Ef1-ZCzcjRc?si=gCI3aKZCtUNjs0hq" %}

The whole playlist "From CAD to Vectary" (9 tutorials):

[https://youtube.com/playlist?list=PLIDfmreWrOG-7qpCKmRoImBaw3jFo3JnN\&si=bDP5LdQ-5D2JzMw5](https://youtube.com/playlist?list=PLIDfmreWrOG-7qpCKmRoImBaw3jFo3JnN\&si=bDP5LdQ-5D2JzMw5)





