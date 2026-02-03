# Export options

Vectary supports exporting projects to a range of widely used 3D file formats. Each format serves different use cases — whether it's for 3D printing, AR, web, or other platforms.

To export a file, go to the **Menu** ➞ **Export**:

<figure><img src="../../.gitbook/assets/image (58).png" alt="" width="375"><figcaption></figcaption></figure>

<table><thead><tr><th width="187.84375">Formats</th><th>Details</th></tr></thead><tbody><tr><td><strong>OBJ</strong> (.obj + .mtl)</td><td><ul><li><strong>Content:</strong> Geometry, basic materials</li><li><strong>Textures:</strong> Separate files</li><li><strong>Best for:</strong> compatibility with most 3D software</li><li><strong>Note:</strong> Does not support animation or lights</li></ul></td></tr><tr><td><strong>DAE</strong></td><td><ul><li><strong>Content:</strong> Geometry, basic materials</li><li><strong>Note:</strong> Can be complex and inconsistent between software</li></ul></td></tr><tr><td><strong>USDZ</strong></td><td><ul><li><strong>Content:</strong> All-in-one AR-ready 3D scene</li><li><strong>Textures:</strong> Embedded</li><li><strong>Supports:</strong> Geometry, materials, animations, lights</li><li><strong>Best for:</strong> Apple AR experiences (iOS, Safari, RealityKit)</li><li><strong>Note:</strong> Single file, lightweight and optimized for AR<br><br>⚠️ USDZ export settings include an option to choose the file type — ASCII or Binary.<br><br>- <strong>ASCII</strong> format saves the data in a human-readable text form, which is useful for debugging and version control. <br><br>- <strong>Binary</strong> format creates smaller files and loads faster, making it more suitable for production and distribution.</li></ul></td></tr><tr><td><strong>GLTF</strong> (.gltf + .bin + textures folder)</td><td><ul><li><strong>Content:</strong> Scene description in JSON</li><li><strong>Textures:</strong> External folder</li><li><strong>Supports:</strong> Geometry, materials, animations, lights, cameras</li><li><strong>Best for:</strong> Web and modern 3D workflows</li><li><strong>Note:</strong> Folder-based format, not ideal for sending as a single file</li></ul></td></tr><tr><td><strong>GLB</strong> (binary glTF)</td><td><ul><li><strong>Content:</strong> All assets packed into a single binary file</li><li><strong>Textures:</strong> Embedded</li><li><strong>Supports:</strong> Geometry, materials, animations, lights, cameras</li><li><strong>Best for:</strong> Web, AR, game engines, and when a single file is needed</li><li><strong>Note:</strong> Compact and easy to share, widely supported</li></ul></td></tr><tr><td><strong>FBX</strong></td><td><ul><li><strong>Content:</strong> Complex scenes with hierarchy</li><li><strong>Textures:</strong> Separate files</li><li><strong>Supports:</strong> Geometry, cameras, lights</li><li><strong>Best for:</strong> Game engines</li><li><strong>Note:</strong> Proprietary format by Autodesk, large file sizes possible</li></ul></td></tr><tr><td><strong>STL</strong></td><td><ul><li><strong>Content:</strong> Pure geometry</li><li><strong>Textures:</strong> Not supported</li><li><strong>Supports:</strong> Geometry data only (triangles)</li><li><strong>Best for:</strong> 3D printing</li><li><strong>Note:</strong> No color, no texture, no animation — just shape</li></ul></td></tr></tbody></table>



Related topics:



[sharing.md](sharing.md "mention")

[augmented-reality-webar.md](../project-settings/augmented-reality-webar.md "mention")

[download-image.md](../design-process/control-bar/download-image.md "mention")

