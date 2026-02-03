---
hidden: true
---

# setTextureData

Sets the [TextureData](../type-definitions.md#texturedata) of a specific [TextureConfig](../type-definitions.md#textureconfig) by its id. A regular [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob) can be passed down as well.

```typescript
setTextureData(
	textureId: string,
	image: TextureData | Blob
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>textureId</td><td>Id of a <a href="../type-definitions.md#textureconfig">TextureConfig</a> that can be retrieved from a <a href="../type-definitions.md#material">Material’s</a> specific texture channel.</td><td><code>string</code></td></tr><tr><td>image</td><td>Object containing the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer">ArrayBuffer</a>, width and height of the texture to be set.</td><td><a href="../type-definitions.md#texturedata">TextureData</a> | <a href="https://developer.mozilla.org/en-US/docs/Web/API/Blob">Blob</a></td></tr></tbody></table>



Usage:

```javascript
const mat = await api.getActiveMaterial('T-Shirt');
const tid = mat.properties.color.id;
const textureData = await api.setTextureData(
	tid,
	{
		image: {ArrayBuffer}
		width: 2048,
		height: 2048,
	}
);
```

