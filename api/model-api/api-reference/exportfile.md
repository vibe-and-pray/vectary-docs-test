---
hidden: true
---

# exportFile

Exports/downloads a 3D file of your [format’s](../type-definitions.md#export3dformats) choosing, of the current scene. [Options](../type-definitions.md#exportoptions) can be added.

```typescript
exportFile(
	format: Export3DFormats,
	options?: ExportOptions
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="228">Description</th><th>Type</th></tr></thead><tbody><tr><td>format</td><td>The 3D format file to <br>export the current scene.</td><td><a href="../type-definitions.md#export3dformats"><code>Export3DFormats</code></a></td></tr><tr><td>options</td><td></td><td><p></p><p><a href="../type-definitions.md#exportoptions"><code>ExportOptions</code></a></p><ul><li><code>fbx</code>: <code>'ASCII'</code>(default) | <code>'Binary'</code></li><li><code>applyParentMatrix</code>: <code>boolean</code></li><li><code>exportOnlyUsedUVs</code>: <code>boolean</code></li></ul></td></tr></tbody></table>



Usage:

```jsx
await modelApi.exportFile('FBX', {fbx: 'Binary'});
```

