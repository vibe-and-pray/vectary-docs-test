# Variants



Variants provide the capability to group multiple objects within a scene, displaying only one object at a time. Switching between these objects is managed through a simple radio button control, allowing rapid transitions between different variations.

<figure><img src="../../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Any type of object can be included within a Variant group - this includes individual objects, groups, Floating UIs, Hotspots, lights, and cameras
{% endhint %}



There are two primary methods to configure user interactions with Variants:



1. Create a [Floating UI](floating-ui/) and add a [Variants](floating-ui/variants-ui.md) (UI element), selecting the desired Variant group as the source.
2. Define an [Interact mode](interactions/) action that triggers the switching of Variants.

{% hint style="info" %}
Variants can serve not only as actions but also as triggers themselves, enabling project behaviors to dynamically change based on the specific variant selected by the end user.
{% endhint %}



{% embed url="https://vimeo.com/713599759" %}



