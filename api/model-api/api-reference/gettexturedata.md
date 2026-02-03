---
hidden: true
---

# getTextureData

Retrieves the [TextureData](../type-definitions.md#texturedata) of specific [TextureConfig](../type-definitions.md#textureconfig) by its id.

```typescript
getTextureData(
	textureId: string
): Promise<TextureData>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>textureId</td><td>Id of a <a href="../type-definitions.md#textureconfig">TextureConfig</a> that can be retrieved from a <a href="../type-definitions.md#material">Material’s</a> specific texture channel.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```javascript
const mat = await api.getActiveMaterial('Box');
const tid = mat.properties.colorConfig.texture.id;
const textureData = await api.getTextureData(tid);
```

Return value:

```jsx
{
    "image": {ArrayBuffer},
    "width": 2048,
    "height": 2048
}
```
