# Ground plane



The [Ground plane](../../design-process/ground-plane.md) is a useful feature for grounding objects and receiving shadows, but it can also impact performance — especially when using dynamic mode.



#### Tips & recommendations



* **Limit the size of the ground plane** – In dynamic mode, a large ground plane increases the area where real-time shadows are calculated. Keep it as small as necessary for better performance.

<figure><img src="../../../.gitbook/assets/image (359).png" alt="" width="375"><figcaption></figcaption></figure>

* **Use baked shadows when possible** – The [**Baked Ground plane**](../../design-process/ground-plane.md#baked-shadow) is a more efficient alternative to dynamic shadows and often produces a more realistic result. In dynamic mode, shadows on the ground plane are calculated in real time, which can slightly affect performance.&#x20;

<figure><img src="../../../.gitbook/assets/image (360).png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="success" %}
When baking the ground plane, a shadow texture is generated. Its resolution is selected during the baking process but can later be reduced in **Preview mode.**
{% endhint %}



