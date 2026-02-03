# Camera



## **Overview**



By default, scene are viewed and edited using a default camera without specific settings. However, multiple custom cameras with various settings can be added, offering enhanced control and visual customization options:<br>

* **Perspective**
* **Field of View**
* **Depth of Field**
* **View Limits**
* **Turntable**
* **Custom Aspect Ratio**



<figure><img src="../../.gitbook/assets/image (392).png" alt=""><figcaption><p>Each camera can be individually customized with its own settings</p></figcaption></figure>

<br>

### Enter/Exit view



After adding a new camera, a view does not activate automatically. To view a scene from a camera’s perspective, select the camera icon in the left panel or click the **`Enter View`** button within the camera settings.\
\
![](<../../.gitbook/assets/image (397).png>)<br>

![](<../../.gitbook/assets/image (399).png>)<br>

Camera adjustments can be made without entering the camera view. Simply select the desired camera and modify its settings in the right panel.





### Focal point



The camera's focal point determines the center of rotation and the focus of view. Use the [Fit View](control-bar/fit-view.md) feature (shortcut key **`A`**) to automatically align the focal point with the center of a selected object.

To adjust the focal point manually, select the camera, then click a focal point on the canvas. The Gizmo tool will then shift control to the focal point, allowing repositioning independently of the camera.



{% embed url="https://screen.studio/share/zuGZEuBY" %}



{% hint style="success" %}
Locking the camera after finding the ideal view prevents accidental position changes\
\
![](<../../.gitbook/assets/image (400).png>)
{% endhint %}



## Camera settings



### **Perspective and Orthographic**



* **Orthographic:** objects maintain consistent size and spacing regardless of their distance
* **Perspective:** mimics human vision, where objects appear smaller as they get farther away

{% embed url="https://vimeo.com/716735984" %}



### Field of view



Adjusting this setting can dramatically alter perceived scale and spatial depth. For instance, small interiors can seem expansive, and objects can appear larger or smaller depending on the setting.

{% embed url="https://vimeo.com/768533144" %}



### Depth of field



Enhances realism by simulating camera focus.

* **Focus offset** — defines the area in clear focus, blurring surrounding areas
* **Intensity** — controls the amount of blur applied

{% embed url="https://vimeo.com/768550518" %}



### **View Limits**



Limits camera interactions such as rotation, zoom, and panning for controlled viewer experience

Setting all parameters to 0 completely restricts scene movement.

Changes can be previewed in Preview mode.

<figure><img src="../../.gitbook/assets/image (269).png" alt="" width="249"><figcaption></figcaption></figure>



### **Turntable**



Enables continuous rotation around the camera's focal point.

<figure><img src="../../.gitbook/assets/image (270).png" alt="" width="239"><figcaption></figcaption></figure>



**Duration** — determines rotation speed

**Easing** — controls smoothness of acceleration; higher values provide smoother transitions

**Resume** — automatically resumes rotation after scene interactions

**Resume Delay** — specifies delay before resuming rotation after interaction





### Custom aspect ratio



Maintains consistent framing when the viewport size decreases, ensuring the distance between the model and the edges of the frame remains constant.

Allows specifying precise aspect ratios individually for each camera, such as **`4:3`**, **`16:9`**, **`1:1`**, **`9:16`**, **`21:9` ,** etc.

{% hint style="info" %}
Also useful for exporting images, enabling downloads in various aspect ratios
{% endhint %}

{% embed url="https://vimeo.com/828154838" %}



