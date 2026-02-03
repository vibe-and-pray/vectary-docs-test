# Reflections

The **Reflections** effect enables surface reflections in the scene, ensuring realistic light behavior.

{% hint style="danger" %}
This effect has a **high** impact on performance. It is recommended to enable it only when necessary or when the scene is highly optimized.
{% endhint %}



{% embed url="https://www.youtube.com/watch?v=y2Vsu6HkRb0" %}

#### Settings:

<figure><img src="../../../.gitbook/assets/image (280).png" alt="" width="563"><figcaption></figcaption></figure>

* **Realtime Samples** – controls the quality of reflections in real-time mode. Higher values improve reflection accuracy but may impact performance.
* **Steady Samples** – adjusts the reflection quality for static renders, producing sharper and more refined reflections.
* **Selection only** – this option allows enabling reflections only for specific objects, groups, or selections, optimizing performance by applying reflections selectively instead of globally -[selections.md](../../other/selections.md "mention")



{% hint style="info" %}
Screen Space Reflections (SSR) are calculated dynamically based on material properties. If roughness and metallic values exceed certain thresholds, SSR is automatically adjusted or disabled to optimize performance for materials where reflections are not essential.
{% endhint %}



