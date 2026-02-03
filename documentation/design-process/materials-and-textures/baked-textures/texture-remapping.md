# Texture remapping

Texture remapping allows converting [ambient-occlusion-texture.md](ambient-occlusion-texture.md "mention") and [lightmap.md](lightmap.md "mention") (proprietary material properties) into basic material settings such as **Roughness** and **Emission**, which are supported in standard 3D formats like **GLB**, **FBX**, **OBJ**, **USDZ**. This ensures that the object retains a similar appearance when exported into a file or viewed in **AR**.



**How to run remapping:**

* for this feature to become available, the object or group must contain **Ambient Occlusion** or a **Lightmap** in any of its materials
* select the desired object or group and right-click to open the context menu
* select the **`Remap AO and LM`**

<figure><img src="../../../../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure>

The time required for the remapping process may vary depending on the complexity of the scene.



**Result:**

* the original object will be hidden
* a copy of the object will appear (If the result is satisfactory, the original object may be deleted, they are not linked)
* the copy of the object will include **Roughness** and **Emission** maps instead of **Ambient Occlusion** and **Lightmap**

{% hint style="info" %}
Brightness and contrast settings can be adjusted for the **Roughness** and **Emission** maps if they do not match the appearance of the **Ambient Occlusion** and **Lightmap**.
{% endhint %}

{% embed url="https://screen.studio/share/jjd2f4V2" %}

