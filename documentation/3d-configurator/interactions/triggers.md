# Triggers

Triggers are key components within interactions, determining when an interaction should activate. Each interaction can contain one or multiple triggers.



<figure><img src="../../../.gitbook/assets/image (47).png" alt="" width="267"><figcaption></figcaption></figure>

Available triggers:

<table><thead><tr><th width="169.0859375">Trigger</th><th>Description</th></tr></thead><tbody><tr><td><strong>On load</strong></td><td>Activates upon project loading.</td></tr><tr><td><strong>On update</strong></td><td>Activates continuously with each frame rendered.<br><mark style="color:red;"><code>May cause performance issues</code></mark></td></tr><tr><td><strong>On click</strong></td><td>Activates upon a click event.</td></tr><tr><td><strong>Mouse enter</strong></td><td>Activates when the mouse cursor enters an area.</td></tr><tr><td><strong>Mouse exit</strong></td><td>Activates when the mouse cursor leaves an area.</td></tr><tr><td><strong>Event listener</strong></td><td>Activates in response to specific events. Learn more: <a data-mention href="events-for-api.md">events-for-api.md</a></td></tr><tr><td><strong>While dragging</strong></td><td>Continuously activates during cursor drag actions. <br><br><strong>Note:</strong> this trigger only detects the cursor interaction - it does not move the object itself. To physically move an object, use the <a data-mention href="actions/transformation.md">transformation.md</a> action and set the target to <code>Pointer</code>.</td></tr><tr><td><strong>While hovering</strong></td><td>Continuously activates when the cursor hovers over an area.</td></tr><tr><td><strong>WebXR (Enter/Exit)</strong></td><td>Activates upon entering or exiting a WebXR session</td></tr></tbody></table>





Triggers can be applied to any 3D object, UI element, or selection within the project.&#x20;

<figure><img src="../../../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="120.3671875">Trigger type</th><th width="458.35546875">Description</th><th>Target</th></tr></thead><tbody><tr><td><strong>Object</strong></td><td><strong>Select any 3D or 2D object as a trigger.</strong><br><br><br>Additional options: <strong>Anywhere</strong> and <strong>Background.</strong></td><td>- Anywhere<br>- Background<br>- Group<br>- 3D objects<br>- 2D objects<br>- Hotspots<br>- Clipping plane<br>- Modifiers<br>- Deformers<br>- 3D text</td></tr><tr><td><strong>Selection</strong></td><td>Selections are useful when objects belong to different groups or cannot be placed in a single group.<br><br>There are two ways to add a selection:<br><br>1. If a selection has already been created, simply choose it from the list.<br><br>2. Select the required objects (minimum two) on the left panel using<br><code>Ctrl</code> and click the <code>+</code> icon.<br><br>Learn more: <a data-mention href="../../other/selections.md">selections.md</a></td><td></td></tr><tr><td><strong>Floating UI</strong></td><td>It is possible to select either the entire Floating UI (Parent) or a specific Floating UI element</td><td>- Entire Floating UI<br>- Image<br>- Button<br>- Divider<br>- Container<br>- Slider<br>- Input<br>- Variants<br>- Materials</td></tr></tbody></table>

