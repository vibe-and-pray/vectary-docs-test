---
hidden: true
---

# mapTextures

Maps two textures together. The top texture is mapped on top of the base texture, with the specified options.

```typescript
mapTextures(
	baseTextureId: string,
	topTextureId: string,
	options?: {
		width?: number;
		height?: number;
		top?: number;
		left?: number;
	}
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>baseTextureId</td><td>Id of a <a href="../type-definitions.md#textureconfig">TextureConfig</a> that can be retrieved from a <a href="../type-definitions.md#material">Material’s</a> specific texture channel.</td><td><code>string</code></td></tr><tr><td>topTextureId</td><td>Id of the top texture that will be applied on top of the base.</td><td><code>string</code></td></tr><tr><td>options</td><td><p>All are optional.</p><p><code>width</code> has preference over <code>height</code> in case they are both specified.</p><p><code>top</code> and <code>left</code> default to 0.</p></td><td>width, height, top, left</td></tr></tbody></table>



Usage:

```jsx
const material = await modelApi.getActiveMaterial('T-shirt');
const newTextureId = await modelApi.addTexture({TextureData | Blob})

await modelApi.mapTextures(material.baseColor.textureConfig.id, newTextureId, {
	top: topInput.value,
	left: leftInput.value,
	width: widthInput.value
});
```
