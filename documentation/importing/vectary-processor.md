---
description: >-
  Use Vectary Processor to streamline the CAD-to-3D workflow with full control
  and local file security
---

# Vectary Processor



## **Overview**



**Vectary Processor** is a standalone desktop application for converting CAD files into **mesh**-based 3D assets for use in Vectary Studio. This tool enables offline optimization and conversion of CAD geometry, ensuring that original files never leave the local machine - a valuable feature for workflows with strict security requirements.

While CAD files can be imported directly into Vectary Studio, **Vectary Processor** offers an alternative workflow focused on enhanced control and optimization. The CAD geometry is converted to mesh during import into the application, allowing full control over mesh quality and structure before uploading to Vectary Studio. The optimized model can then be uploaded with a single click, becoming editable geometry ready for further refinement.



{% hint style="success" %}
#### Operating system support

The application is available for **Windows 11** and **macOS**
{% endhint %}



{% hint style="success" %}
#### Where to download

To request access to Vectary Processor, please contact the Vectary Sales team - [https://www.vectary.com/business-contact/](https://www.vectary.com/business-contact/)
{% endhint %}





## Access Token



When opening Vectary Processor for the first time, an access token is required. The token is tied to the user's profile and can be retrieved from the Vectary Dashboard:



1. Go to https://www.vectary.com/dashboard/
2. Click on the profile picture in the top-right corner
3. Select “Copy My Token”\
   \
   ![](<../../.gitbook/assets/image (461).png>)<br>
4. Paste the token into the input field in the Vectary Processor app\
   \
   ![](<../../.gitbook/assets/image (460).png>)<br>

Once added, the token does not need to be re-entered after closing the application.





## Import



* Supports `STEP` / `STP` file formats
* Drag and drop files directly into the app or use the import dialog
* All imported **NURBS** geometry is automatically converted into **mesh geometry**
* Processing time varies depending on file complexity

\
Upon import, the application automatically sets:<br>

* Linked geometries as in the original CAD file
* Box mapping for each object for easier material workflow
* Pivot point centered for each object





## Navigation



Navigation behavior is identical to [Vectary Studio:](../getting-started/scene-orientation.md)<br>

* **Zoom**: scroll wheel (mouse) / two-finger scroll (touchpad)
* **Rotate**: left-click and drag (mouse) / one-finger drag (touchpad)
* **Pan**: right-click and drag (mouse) / two-finger drag (touchpad)
* **Deep Select**: hold **Ctrl** (Windows) or **Cmd** (macOS) and click to select deeper objects in the hierarchy
* **Polygon Highlighting**: selecting an object displays its polygonal mesh



{% hint style="info" %}
**Tip:** reducing the size of the Vectary Processor window can improve 3D preview performance
{% endhint %}





## Bottom toolbar



### Mesh optimization



After processing, geometry appears with default **medium** mesh quality.&#x20;

<div align="left"><figure><img src="../../.gitbook/assets/image (462).png" alt="" width="528"><figcaption></figcaption></figure></div>

#### Optimization options:



* **Easy**: use the slider to set triangle density (displayed in tooltip)<br>
* **Advanced**: configure individual settings:<br>
  * **Linear deflection**: maximum deviation between NURBS and mesh
  * **Angular deflection**: maximum angle between mesh polygons
  * **Min edge size**: minimum allowed polygon edge length\
    \
    ![](<../../.gitbook/assets/image (463).png>)





### Selections

<div align="left"><figure><img src="../../.gitbook/assets/image (464).png" alt="" width="563"><figcaption></figcaption></figure></div>

* **Select similar**: selects surfaces or volumes with similar properties
* **Select instances**: selects all instances of the selected object. Vectary Processor identifies and automatically links all instanced objects, ensuring they remain synchronized during optimization.
* **Select all**: selects all objects in the scene
* **Invert selection**: inverts current selection
* **Select hidden objects**: selects objects that are enclosed within or obscured by other geometry and therefore not visible from the camera’s perspective. This is particularly helpful for optimizing scenes: users can easily identify and remove hidden objects that serve no purpose in the final visualization or interaction. Cleaning up these unnecessary elements can significantly enhance both performance and loading times.





### Object settings

<div align="left"><figure><img src="../../.gitbook/assets/image (465).png" alt="" width="563"><figcaption></figcaption></figure></div>

* **Rotate scene**: toggles object rotation across six axis orientations
* **Separate selection**: separates merged geometry into individual objects
* **Merge selection**: merges selected objects into one
* **Magic merge**: merges the lowest-level unlinked children in the hierarchy







## Top left toolbar

<div align="left"><figure><img src="../../.gitbook/assets/image (466).png" alt="" width="254"><figcaption></figcaption></figure></div>

* <img src="../../.gitbook/assets/image (469).png" alt="" data-size="line"> **Object list**: toggle visibility
* <img src="../../.gitbook/assets/image (470).png" alt="" data-size="line"> [**Fit view**](../design-process/control-bar/fit-view.md): centers selected object in view (Shortcut: <kbd>**A**</kbd>)
* <img src="../../.gitbook/assets/image (471).png" alt="" data-size="line"> **Delete**: removes selected object (Shortcut: <kbd>**Delete**</kbd> or <kbd>**Backspace**</kbd>)
* <img src="../../.gitbook/assets/image (472).png" alt="" data-size="line"> **Isolate**: hides all other objects except the selection (Shortcut: <kbd>**I**</kbd>)
* <img src="../../.gitbook/assets/image (473).png" alt="" data-size="line"> **Exit isolate**: exits isolation mode and shows all objects





## Upload to Vectary Studio



{% hint style="danger" %}
#### Projects in Vectary Processor are **not saved** automatically

All changes made during the optimization process remain local and are not preserved unless the project is manually uploaded. Uploading is done via the **`Upload to Vectary`** button, which transfers the current file to the Vectary Dashboard. Each upload generates a separate project entry, ensuring that the optimized version is securely stored and available for future editing or collaboration.
{% endhint %}



To save a project:<br>

1. Click **`Upload to Vectary`** (top-right corner)
2. Name the project
3. Select a workspace
4. Choose a folder<br>

{% hint style="info" %}
**Tip:** each uploaded file becomes an individual 3D asset in the Vectary Dashboard. Projects can be assembled later in the Workspace tab in Vectary Studio.
{% endhint %}





## Tabs



Multiple projects can be opened simultaneously in separate tabs.

<div align="left"><figure><img src="../../.gitbook/assets/image (467).png" alt="" width="411"><figcaption></figcaption></figure></div>

{% hint style="info" %}
**Tip:** continue working on one project while others are processing in background tabs
{% endhint %}





## Optimization tips



Optimized scenes are essential for achieving fast loading times and smooth performance in web environments across all platforms. As the final output from Vectary Processor is intended for use on the web, careful optimization ensures efficient rendering and a responsive user experience. Mesh density is a key factor in this process, as overly complex geometry can negatively impact performance. Reducing triangle count where possible helps maintain visual quality while significantly improving scene efficiency.



<div align="left"><figure><img src="../../.gitbook/assets/image (468).png" alt="" width="267"><figcaption></figcaption></figure></div>

### **Mesh Density**



* Recommended range: 200k–500k Linked Triangles
* Keep triangle count as low as possible
* Use mesh optimization slider to control density
* Prioritize detail for objects closer to the camera; reduce detail for background objects



### **Object count**



* Recommended maximum: 500 objects
* Use **`Merge selection`** or **`Magic merge`** to reduce object count
* Only merge objects sharing the same material and behavior



