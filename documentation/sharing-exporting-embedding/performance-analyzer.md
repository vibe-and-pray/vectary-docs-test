---
description: Scene performance analyzer is there to assist you in optimizing your project
---

# Performance analyzer



## Overview



Optimizing a project is essential for maintaining good performance. The **Preview mode** provides insights into how optimized the scene is and offers tools for quick improvements:



* Total number of objects, source geometries, and polygons
* Number of textures and their resolution (resolution can be changed directly here)
* Number of interactions and animations (unused ones can be removed instantly)
* Project loading time and total size
* Performance metrics such as FPS and factors that affect it



{% embed url="https://screen.studio/share/F3c1OBPO" %}

Hover over each icon to see more details:

<figure><img src="../../.gitbook/assets/image (63).png" alt="" width="496"><figcaption></figcaption></figure>

## Optimization Indicators



* <mark style="color:red;">R</mark><mark style="color:red;">**ed warning icon**</mark> indicates a metric that needs optimization. It's always a good idea to keep values low where possible.
* <mark style="color:green;">G</mark><mark style="color:green;">**reen check icon**</mark> means the value is acceptable, but it doesn't always guarantee good performance/loading time. For example, having many `2048×2048` textures can still negatively impact loading time and should ideally be optimized (either reduced to the lowest practical resolution or removed entirely if it doesn't provide significant visual improvement).

Learn more about optimization here: [optimizing-a-shared-project](optimizing-a-shared-project/ "mention")



<div align="left"><figure><img src="../../.gitbook/assets/image (61).png" alt="" width="234"><figcaption></figcaption></figure></div>



## Metric Descriptions



* **Total objects** – Total number of objects in the project (including hidden ones)
* **Source Geometries** – Number of objects with unique geometry
* **Polygons** – Total polygon count in the project<br>
* **Textures** – Number of textures currently in use (unused textures are not listed)
  * Texture resolution can be changed directly here<br>
* **Interactions** – "Unreferenced" interactions are linked to deleted objects. Click `Clear unreferenced interactions` to remove them
* **Animations** – Displays animation tracks with no keyframes. Use `Clear empty animations` to delete them<br>
* **Loading time** – Click the icon <img src="../../.gitbook/assets/image (64).png" alt="" data-size="line"> to calculate scene size and estimated project loading time
* **Performance** – Click the icon <img src="../../.gitbook/assets/image (65).png" alt="" data-size="line"> to measure FPS (based on your device) and identify performance-impacting factors





