# Simplify

Reduces the complexity of an object's geometry, optimizing its topology while maintaining overall shape integrity.&#x20;

{% hint style="warning" %}
Note that very high-polygon models may cause the browser tab to become unresponsive
{% endhint %}

{% embed url="https://vimeo.com/713999009" %}

{% hint style="success" %}
To improve performance in Studio, it is recommended to bake the deformer whenever possible to avoid unnecessary recalculations.\
\
![](<../../../../.gitbook/assets/image (454).png>)
{% endhint %}

{% hint style="danger" %}
#### API-related warning

In a published project, objects under a **Simplify** modifier are baked - as a result, these objects are no longer individually targetable through the API.
{% endhint %}



