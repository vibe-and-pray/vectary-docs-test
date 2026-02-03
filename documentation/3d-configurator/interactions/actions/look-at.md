# Look at



## Overview



The **Look at** action enables automatic rotation of an object toward a designated target. It supports a wide range of use cases - from aligning individual elements to the viewer, to creating coordinated behaviors across multiple grouped objects. This action allows objects to follow other elements, respond to the viewer’s perspective, or dynamically track movement.



<figure><img src="../../../../.gitbook/assets/image (491).png" alt="" width="563"><figcaption></figcaption></figure>



## Usage examples



1. **3D UI in VR**: recreate user interfaces using 3D objects instead of Floating UI or Hotspots, which are not supported in WebXR for **VR Glasses**. \
   \
   <a href="https://app.vectary.com/p/5wabtnqnG2e87YqWnKYbi8" class="button secondary">Demo</a>\
   \
   <br>
2. **Mechanical simulation**: use **Look at** to simulate components like pistons following each other.\
   \
   <a href="https://app.vectary.com/p/3t4llKFxljwglg6pZhos58" class="button secondary">Demo</a>\
   \
   <br>
3. **Pointer tracking**: rotate an object to face the mouse cursor (works only on desktop devices).\
   \
   <a href="https://www.vectary.com/p/4AwoVLt4mu7NNUUCZ1qpIw" class="button secondary">Demo</a>\
   \
   <br>
4. **Selection-based targeting**: apply the action to a [selection](../../../other/selections.md) of objects. \
   \
   <a href="https://app.vectary.com/p/0dUBxocruoaBzkAX1A3aEV" class="button secondary">Demo</a>\
   <br>



## Parameters



* **Object -** specifies which object should rotate<br>
* **Target -** defines the target to look at. This can be another object, the camera view, or the pointer (on desktop devices).\
  <br>
* <mark style="color:red;">**Billboard**</mark>**&#x20;-** when enabled, the object is aligned perpendicular to the camera view instead of pointing directly at the camera. Useful for creating flat elements that always face the screen.\
  \
  ![](<../../../../.gitbook/assets/image (493).png>)\
  \
  <a href="https://app.vectary.com/p/5Ai5PxAdApALCci1QDZapF" class="button secondary">Demo</a>



* **Track axis** - determines which local axis of the object should face the target. By default, this is set to the <mark style="color:blue;">**`Z`**</mark> axis.
* **Up axis** - defines the up direction for the object. **Must be different from the track axis.**\
  \
  <a href="https://app.vectary.com/p/12xTaTPJqVItsKyHq9kAz6" class="button secondary">Demo</a>





* **Ease type —** controls the animation easing when the object rotates
* **Duration —** specifies the time (in seconds) it takes to rotate toward the target
* **Delay —** optional delay before the action starts





## Combining with Transformation



In some cases, the **Look at** action can be combined with the **Transformation** action. Note that Transformation by default copies the target's rotation. To achieve a custom orientation while preserving independent control, rotation can be disabled in the Transformation action [using the rotation icon toggle](https://help.vectary.com/documentation/3d-configurator/interactions/actions/transformation#disabling-transformations).

