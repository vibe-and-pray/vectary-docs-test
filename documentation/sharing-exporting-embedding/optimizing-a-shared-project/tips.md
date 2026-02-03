# Tips

### Final checks before sharing a project



Before sharing or embedding your project, it's important to make a few final adjustments to ensure the best performance and user experience.

These small details can greatly enhance how your project is experienced when shared:



1.  **Avoid covering the entire scene with objects**\
    \
    If an object fills the entire background, the whole screen must be rendered. However, if the background is set using the [**Background settings**](../../design-process/background.md), only the visible portion of the object is rendered — which can reduce rendering load significantly (e.g., 10% vs. 100%).

    Use the built-in background color options instead of placing a Plane or Backdrop behind objects. Background settings have almost no performance impact.\
    <br>
2.  **Adjust the center of rotation**\
    \
    Set a custom pivot point for the scene to control how it rotates in the viewer. The most precise method is to manually adjust the pivot position of the camera - [#focal-point](../../design-process/camera.md#focal-point "mention")

    Alternatively, use the [**Fit View**](../../design-process/control-bar/fit-view.md) function (`A` key) to automatically focus the camera on an object — this sets the rotation center accordingly. This applies both in Studio and the Viewer. \
    <br>
3. **Tweak final presentation settings**\
   \
   Review and adjust various viewer settings such as:<br>
   * [Turntable rotation](../../design-process/camera.md#turntable)
   * [Loading screen appearance](../../project-settings/loading-screen.md)
   * [Mouse control behavior](../../project-settings/mouse-controls.md)
   * [Camera constraints and movement limits](../../design-process/camera.md#view-limits)<br>

