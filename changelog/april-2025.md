# April 2025



### April 24



{% tabs %}
{% tab title="Features" %}
{% hint style="success" %}
## April 24



* Added option to disable position, rotation, and scale in the `Transformation` action
* Improved export of **Ambient Occlusion** map
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
#### April 24



* Fixed various bugs related to keyframes
* Minor bug fixes
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Improved export of **Ambient Occlusion** map

For USDZ files (and therefore for AR), Ambient Occlusion unfortunately doesn't always get exported. This may be improved in the future. However, we recommend using the Texture Remapping feature, which allows you to convert the AO map into a supported texture. Read more here: [https://help.vectary.com/documentation/design-process/materials-and-textures/baked-textures/texture-remapping](https://help.vectary.com/documentation/design-process/materials-and-textures/baked-textures/texture-remapping)
{% endhint %}

{% hint style="info" %}
#### Added option to disable position, rotation, and scale in the `Transformation` action

[https://help.vectary.com/documentation/3d-configurator/interactions/actions/transformation#disabling-transformations](https://help.vectary.com/documentation/3d-configurator/interactions/actions/transformation#disabling-transformations)
{% endhint %}
{% endtab %}
{% endtabs %}





### April 9



{% tabs %}
{% tab title="Features" %}
{% hint style="success" %}
## April 9



* Added option to define **units** for **imported** files
* Added ability to download `USDZ` file via API
* Improved support for **skeletal animation** in AR on iOS
{% endhint %}
{% endtab %}

{% tab title="Bug fixes" %}
{% hint style="success" %}
#### April 9



* Fixed bug where some animated textures were deleted after running performance check
* Fixed problem causing `Floating UI` to disappear after moving it to another group
* Fixed issue where custom swatch images disappeared after the object was moved in the object list
* Fixed bug where applying transformations to a single object affected all instance objects
* Minor bug fixes
{% endhint %}
{% endtab %}

{% tab title="Details" %}
{% hint style="info" %}
#### Added option to define **units** for **imported** files

[https://help.vectary.com/documentation/getting-started/units#file-import](https://help.vectary.com/documentation/getting-started/units#file-import)
{% endhint %}

{% hint style="info" %}
#### Improved support for **skeletal animation** in AR on iOS

Previously, not all skeletal animations worked correctly in AR — this has now been fixed. This also applies to USDZ file export.
{% endhint %}
{% endtab %}
{% endtabs %}



