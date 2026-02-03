# Light and shadows



[Local lights](../../design-process/design-mode/light-sources.md) can enhance realism and atmosphere, but they can also significantly impact performance — especially when shadows are enabled.



#### Tips & recommendations



* **Try HDRI adjustments first** – if a scene lacks lighting, start by trying different [**HDRI environments**](../../design-process/environment.md). And make sure to fine-tune HDRI parameters for optimal lighting results. \
  Note that **Environment Intensity** can be set above 100% by manually entering the value.\
  <br>
* **Be mindful with shadows** – by default, local lights have shadows disabled. Enable them only when necessary, and only on the specific lights where shadows add a clear visual benefit.\
  <br>
* **Prefer directional or spotlight sources** – these light types are generally more efficient in terms of shadow rendering and performance.\
  <br>
* **Limit shadow-heavy light types** – avoid using more than one **Point** or **Rectangle** light with shadows enabled in a scene. These types of lights are more taxing on performance.



