# September 2025





### September 16



{% tabs %}
{% tab title="Features" %}
{% hint style="success" %}
#### September 16



* Added AI-based [3D model generation from image](../documentation/other/image-to-3d-model/)
{% endhint %}
{% endtab %}
{% endtabs %}





### September 4



{% tabs %}
{% tab title="Features" %}
{% hint style="success" %}
#### September 4



* Added new [Embed](../documentation/3d-configurator/floating-ui/embed.md) element to [Floating UI](../documentation/3d-configurator/floating-ui/) for embedding external code and links directly into Vectary project
{% endhint %}
{% endtab %}
{% endtabs %}





### September 2



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### September 2



* Improved [interactions](../documentation/3d-configurator/interactions/) optimization, which led to improved performance in projects with performance problems caused by interactions
* Improved resolution and performance in [WebXR](../documentation/project-settings/webxr-beta.md)
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
#### September 2



* Fixed issue preventing use of [variables](../documentation/3d-configurator/variables-and-expressions/) for [Normal map](../documentation/design-process/materials-and-textures/basic-materials/normal-map.md) and [Opacity](../documentation/design-process/materials-and-textures/basic-materials/opacity.md) properties
* Fixed bug preventing AR file generation in Studio when a video texture was used in [Emission](../documentation/design-process/materials-and-textures/basic-materials/emission.md), [Roughness](../documentation/design-process/materials-and-textures/basic-materials/roughness.md), or [Metalness](../documentation/design-process/materials-and-textures/basic-materials/metalness.md) properties
* Fixed bug where AR could sometimes fail to open on the first attempt if AR files were generated in the [dashboard preview](../documentation/getting-started/dashboard.md#preview-mode)
* Fixed bug where [aspect ratio](../documentation/design-process/camera.md#custom-aspect-ratio) was not applied when switching cameras via interaction
* Fixed bug causing **Hue** value to change when adjusting color in the palette
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Performance and WebXR improvements



We’ve improved how [interactions](../documentation/3d-configurator/interactions/) are handled, resulting in smoother performance for projects that previously struggled with too many interactions or heavy calculations. Today’s improvement has significantly increased FPS not only when running interactions, but also while rotating the camera and in [UI](../documentation/3d-configurator/floating-ui/) responsiveness. Projects that used to lag due to interactions should now feel noticeably faster and smoother! :tada:

This improvement has also boosted performance in the [WebXR](../documentation/project-settings/webxr-beta.md) experience.\
In addition, we’ve improved resolution in WebXR, so projects that previously opened in low resolution should now appear much sharper.
{% endhint %}
{% endtab %}
{% endtabs %}





