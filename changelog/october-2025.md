# October 2025





### October 21



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### October 21



* Improved animation optimization in USDZ (AR, export)
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
### October 21



* Fixed issue where [AI-generated object](../documentation/other/image-to-3d-model/) was not displayed in [AR](../documentation/project-settings/augmented-reality-webar.md) (iOS)
* Fixed bug where animated [3D text](../documentation/design-process/design-mode/3d-text.md) was displayed incorrectly in [AR](../documentation/project-settings/augmented-reality-webar.md)
* Fixed bug where duplicating an object in [Variants](../documentation/3d-configurator/variants.md) caused it to disappear
* Fixed incorrect value increment when modifying `Offset` in texture transformation
* Fixed synchronization of object name in the `Source` field of [Materials](../documentation/3d-configurator/floating-ui/materials-ui.md) after renaming
{% endhint %}
{% endtab %}
{% endtabs %}





### October 9



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### October 9



* Added ability to define dragging behavior in [WebXR](../documentation/project-settings/webxr-beta.md) headset (move, rotate, or both)
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
### October 9



* Fixed multiple issues within Offline Viewer app
* Fixed **Array** [modifier](../documentation/design-process/design-mode/modifiers/) breaking `UV1`, resulting in incorrect [AO/LM](../documentation/design-process/materials-and-textures/baked-textures/) maps
* Fixed issue where non-referenced [interactions](../documentation/3d-configurator/interactions/) were not detected in the [analyzer](../documentation/sharing-exporting-embedding/performance-analyzer.md)
* Fixed issue where removing animation name also removed the text field, preventing adding a new name
* Fixed issue where renamed object was not updated on the [timeline](../documentation/3d-configurator/animations.md#timeline)
* Fixed issue where removing an object from the [timeline](../documentation/3d-configurator/animations.md#timeline) deleted it from the scene
* Fixed issue where using an [expression](../documentation/3d-configurator/variables-and-expressions/#expressions) in overlay input was not saved
{% endhint %}
{% endtab %}
{% endtabs %}





### October 3



{% tabs %}
{% tab title="Improvements" %}
{% hint style="success" %}
### October 3



* Added automatic scroll of the Objects panel when selecting an object on canvas
* Added parameter to set [`Offset`](../documentation/design-process/decals.md#editing-decals) for decals
* Improved performance of the [interactions](../documentation/3d-configurator/interactions/) list
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
### October 3



* Fixed bug where [decals](../documentation/design-process/decals.md) were not attached to objects when scale value was too large
* Fixed bug that prevented changing transformation settings for textures [imported from Figma](../documentation/importing/figma-frames-import.md)
* Fixed bug where duplicating [Floating UI](../documentation/3d-configurator/floating-ui/) sometimes resulted in doubled elements
* Fixed bug where hidden objects in Array [modifier](../documentation/design-process/design-mode/modifiers/) were still visible in preview and shared link
* Fixed bug that caused [Floating UI](../documentation/3d-configurator/floating-ui/) flickering (under certain settings) in project [preview on Dashboard](../documentation/getting-started/dashboard.md#preview-mode)
* Fixed issue causing incorrect transformation of animated objects in [AR](../documentation/project-settings/augmented-reality-webar.md) on iOS for objects with non-uniform scaling
* Fixed several issues that caused project saving errors
* Minor bug fixes
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Offset for decals

* Sometimes decals could flicker (usually when zooming out). Now this can be fixed with the new [Offset parameter](../documentation/design-process/decals.md#editing-decals) in the decal settings (note that this option appears only after you attach the decal to an object).
{% endhint %}

{% hint style="info" %}
#### Improved performance of the Interactions list

* Previously, with a large number of [interactions](../documentation/3d-configurator/interactions/) in a project, working with the list (for example grouping or ungrouping) could cause long delays. We made some improvements and now it works much faster.
{% endhint %}

{% hint style="info" %}
#### Automatic scroll of Objects panel

* A small but very welcome improvement – when selecting an object on the canvas, the panel on the left now automatically scrolls to the selected object.
{% endhint %}
{% endtab %}
{% endtabs %}



