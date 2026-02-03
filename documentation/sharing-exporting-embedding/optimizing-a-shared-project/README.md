# Optimizing a shared project



## Overview



Vectary is a powerful web-based tool capable of producing high-quality, realistic 3D scenes. But since projects are rendered directly in the browser, optimization plays a critical role in ensuring smooth performance and fast load times across all devices.

This page outlines key recommendations to help improve scene performance and loading time.



## Why optimization matters



There are two main areas where optimization makes a big difference:



**1. Performance**

Just like in video games, real-time 3D scenes in Vectary can perform differently depending on the device. While many optimization tasks are handled automatically, some require manual tuning — especially if the scene needs to run smoothly on lower-end devices like mobile phones or older laptops. \
<br>

**2. Loading Time**

When embedding a scene into a website, fast loading is essential. Ideally, the scene should load within **2 to 3 seconds**.&#x20;

{% hint style="success" %}
For the best results, try to keep the **embed size under 5MB**, with a hard maximum of **10MB**
{% endhint %}



## Performance check



* Always preview the scene on low-end devices to ensure accessibility for all users.\
  <br>
* Use the **Preview mode** to test performance and loading — it includes a built-in performance analyzer - [performance-analyzer.md](../performance-analyzer.md "mention")\
  <br>
* Keep textures, polygon count, and effects optimized (see detailed recommendations below):\
  <br>
  * [geometry.md](geometry.md "mention")
  * [textures.md](textures.md "mention")
  * [materials.md](materials.md "mention")
  * [effects.md](effects.md "mention")
  * [light-and-shadows.md](light-and-shadows.md "mention")
  * [hdri.md](hdri.md "mention")
  * [ground-plane.md](ground-plane.md "mention")
  * [tips.md](tips.md "mention")





## Tutorials



{% embed url="https://youtu.be/Qx5SYW2F92M" %}

