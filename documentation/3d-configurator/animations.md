# Animations

## Overview



Vectary’s animation system is based on **keyframes**, allowing for precise control over object transformations within a structured timeline. The animation workflow is built around a timeline where keyframes define changes over time. \
\
To animate objects, switch to **Animate mode.**

<figure><img src="../../.gitbook/assets/image (436).png" alt=""><figcaption></figcaption></figure>



## Timeline



The **timeline** is the primary interface for managing animations in Vectary. It provides a visual representation of keyframes along a linear time axis, allowing precise control over animation timing and transitions. The timeline enables to set, move, and edit keyframes, adjust interpolation, playback type, and structure animations efficiently.

<figure><img src="../../.gitbook/assets/image (445).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
The height of the timeline can be adjusted by dragging its edge to expand or contract the view
{% endhint %}



### **Master Handlers & Keyframes**



The timeline displays only two keyframes by default - the **first** and **last** - called **Master Handlers**.&#x20;

<figure><img src="../../.gitbook/assets/image (437).png" alt=""><figcaption></figcaption></figure>

All intermediate keyframes are contained within the **master group** and can be accessed by clicking the expand icon or double-clicking the grey line.

<figure><img src="../../.gitbook/assets/image (438).png" alt=""><figcaption><p><strong>master group</strong></p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (439).png" alt=""><figcaption><p>intermediate keyframes inside master group</p></figcaption></figure>

{% hint style="success" %}
Dragging a **Master Handler** scales all keyframes proportionally
{% endhint %}



#### **Keyframes**



* To record data into a keyframe, move the **playhead** to the desired position and transform the object on the canvas. Each transformation (**position**, **rotation**, **scale**) is automatically recorded into a keyframe at the playhead's position.
* To overwrite an existing keyframe, position the playhead over the keyframe and modify the object's transformation. The new transformation values will replace the previous ones in that keyframe.
* Keyframes can be moved individually or in groups. To select multiple keyframes, either hold **Shift** and click on them or drag with the left mouse button to select a range of keyframes.

<figure><img src="../../.gitbook/assets/select keys.gif" alt=""><figcaption></figcaption></figure>



### **Interpolation**



Interpolation controls how animation transitions between keyframes.&#x20;

To change interpolation, select at least one keyframe and choose the desired method.

<figure><img src="../../.gitbook/assets/image (442).png" alt=""><figcaption></figcaption></figure>

Available interpolation types:



* **Ease Auto** — Automatically adjusts smoothing for the best transition.
* **Ease In & Out** — Starts slowly, accelerates, and then decelerates toward the end.
* **Ease In** — Starts slowly and then moves at a constant rate.
* **Ease Out** — Starts immediately and slows down toward the end.
* **Linear** — Moves at a constant speed without acceleration.
* **Constant** — Instantly switches states without transition.





### **Animation tabs**



Multiple **tabs** can be created above the timeline, each representing a separate animation with its own timeline.

<figure><img src="../../.gitbook/assets/image (440).png" alt=""><figcaption></figcaption></figure>

* Tabs can be rearranged by dragging them
* Right-clicking on a tab opens a context menu with options to **duplicate, delete, or invert** the animation
* **Inverting** reverses the order of keyframes, creating a mirrored animation
* Each animation tab can be controlled individually using the [animation.md](interactions/actions/animation.md "mention") interaction
* Tab can be renamed by double-clicking on it





### **Timeline scale**



The timeline scale controls the level of detail in the animation timeline:<br>

* **100%** — 1 grid step = 0.1s
* **10%** — 1 grid step = 0.01s
* **1000%** — 1 grid step = 1s<br>

<figure><img src="../../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>



### **Playhead (CTI)**



The **playhead** is a movable indicator that represents the current position within the animation timeline. It determines where new keyframes are recorded and serves as a reference point for editing animation sequences.

<figure><img src="../../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure>

* Moving the playhead allows previewing animation states at different points in time.
* Any transformation applied to an object while the playhead is positioned on the timeline automatically creates or updates a keyframe.
* The playhead can be dragged along the timeline to navigate through the animation.
* Clicking on the timeline moves the playhead to that position.





### Mark In & Mark Out



Mark In and Mark Out define the playback range of an animation. This range determines which part of the animation is played, but it does not affect the placement or existence of keyframes - keyframes can exist outside the Mark In/Out range and remain unchanged.

<figure><img src="../../.gitbook/assets/image (444).png" alt=""><figcaption></figcaption></figure>

* **Mark In** defines the start of the animation.
* **Mark Out** defines the end of the animation.
* Both can be moved independently by dragging.
* Adjusting Mark In/Out does not affect keyframes; keyframes outside this range simply won't play.
* **Double-click** on Mark In/Out to snap to the first or last keyframe.
* **Hold Shift** while dragging to scale the animation proportionally.





### Playback type



Defines how the animation plays back.



* **Single** — Plays once and stops
* Loop — Repeats continuously\
  \
  ![](../../.gitbook/assets/repeat.gif)
* Ping-pong — Plays forward, then reverses\
  \
  ![](<../../.gitbook/assets/ping pong.gif>)







## Base state



The **Base State** represents the object's original transformation in **Design Mode**. Each keyframe modifies specific transformation parameters, but any parameters not animated will always follow the Base State.



## Importing



<table><thead><tr><th width="194.609375">Formats</th><th>Animation type</th></tr></thead><tbody><tr><td><strong>GLTF</strong></td><td><ul><li>Transform animations (position, rotation, scale)</li><li>Skeletal animations</li></ul></td></tr><tr><td><strong>GLB</strong></td><td><ul><li>Transform animations (position, rotation, scale)</li><li>Skeletal animations</li></ul></td></tr><tr><td><strong>FBX</strong></td><td><ul><li>Transform animations (position, rotation, scale)</li><li>Skeletal animations</li></ul></td></tr></tbody></table>



### Skeletal animations

Skeletal animations can be imported. Bones can be manipulated and modified, allowing for animation, interaction, and transformation. However, creating bones from scratch and linking them to geometry is **not yet supported** but planned for future updates.



## Exporting



Formats that support animation export:<br>

* **GLTF**
* **GLB**
* **USDZ**





## Shortcuts



For shortcuts to function, the cursor must be in the **timeline area.**

<table><thead><tr><th width="174.43359375">Shortcut</th><th>Action</th></tr></thead><tbody><tr><td><strong>Spacebar</strong></td><td>Play/pause from the current position.</td></tr><tr><td><strong>Enter</strong></td><td>Play from the beginning.</td></tr><tr><td><strong>Left Arrow</strong></td><td>Move the playhead left.</td></tr><tr><td><strong>Right Arrow</strong></td><td>Move the playhead right.</td></tr><tr><td><strong>Delete</strong></td><td>Remove the selected keyframe.</td></tr></tbody></table>





## Tutorials

{% embed url="https://youtu.be/j0QErgtVPSg?si=zkLJmK6VeduvYQIF" %}

{% embed url="https://youtu.be/XjUPKHIYs7E?si=np13LBQbwuiEJSZ9" %}

{% embed url="https://youtu.be/dohwb97yRI0?si=aOTLN6IhziBv_cxV" %}

{% embed url="https://youtu.be/TWxZzwvhk7s?si=Y9pVcM-pPtDdPyti" %}

{% embed url="https://youtu.be/3cNRlFBKSbY?si=2MlWW_WDlIoSLJbK" %}

{% embed url="https://youtu.be/9L16kocsUTQ?si=vpTRABku1_UnbzCF" %}

