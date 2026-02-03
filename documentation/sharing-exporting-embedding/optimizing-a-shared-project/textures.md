# Textures



Textures are often the main reason for large project sizes and slow loading times. Using high-resolution textures or too many of them can also lead to memory issues, especially on mobile devices or low-performance hardware.



Some textures may offer little to no visual benefit while significantly increasing project size. These should either be removed or their resolution reduced to the lowest acceptable level.



All active textures can be reviewed and adjusted in [**Preview mode**](../performance-analyzer.md), where resolution changes can be applied globally. Textures can also be edited individually in the material or environment settings where they're used.



#### Tips & recommendations



* **Use textures only when necessary.** In some cases, adjusting the geometry may be more efficient than simulating detail through textures.\
  <br>
* **Reduce resolution wherever possible.** For example, lowering a texture from `2048×2048` to `512×512` often makes little visual difference but improves performance and loading time significantly.\
  <br>
* **Choose efficient formats.** Use **JPG** or **SVG** instead of **PNG**, unless transparency is required. PNG files are typically heavier and less optimized for web.\
  <br>
* **Avoid GIFs.** For animations, use **Lottie** or **MP4** formats — both are far better optimized for performance and file size.\
  <br>
* **Test on mobile devices.** Preview the scene on a phone or low-spec device to check if textures cause memory or rendering issues.



