# January 2026





### January 15



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### January 15



* Added ability to select different AI models for [3D generation](../documentation/other/image-to-3d-model/)
* Added **`Scale factor`** parameter to [AR](../documentation/project-settings/augmented-reality-webar.md) and [export](../documentation/sharing-exporting-embedding/export-options.md) settings&#x20;
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
### January 15



* Fixed bug where projects containing videos failed to load on iPhone
* Fixed bug that prevented creating a new Event in the [**Send Event**](../documentation/3d-configurator/interactions/actions/send-event.md) action
* Fixed shading issue that could occur on objects with bones[^1]
* Fixed issue where camera position changed when a project was taken over by another workspace member
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### AI generation: image to 3D&#x20;



* The `image-to-3D` generation feature has been expanded. Previously, generation was available with a single AI model, now you can choose from multiple. \
  \
  More details: [image-to-3d-model](../documentation/other/image-to-3d-model/ "mention")
{% endhint %}

{% hint style="info" %}
#### **Scale factor**



* We’ve added a **Scale factor** parameter that makes it easier to adjust an object’s scale for AR and during export.\
  Instead of resizing the entire project to match the desired real-world size in augmented reality, you can now simply specify how much larger or smaller the object should be as a percentage.\
  \
  ![](../.gitbook/assets/image.png)
{% endhint %}
{% endtab %}
{% endtabs %}





[^1]: skeletal animation
