# getTextureData \[new]

#### getTextureData

Returns the raw image data of a texture.

#### Signature

```typescript
getTextureData(textureId: string): Promise<TextureData>
```

#### Parameters

| Name        | Type     | Required | Description       |
| ----------- | -------- | -------- | ----------------- |
| `textureId` | `string` | Yes      | ID of the texture |

#### Returns

`Promise<TextureData>` — Texture image data.

```typescript
type TextureData = {
  image: ArrayBuffer;
  width: number;
  height: number;
};
```

#### Usage

```javascript
// Get texture ID from material
const material = await api.getActiveMaterial("Chair");
const textureId = material.baseColor.textureConfig.id;

// Get texture data
const data = await api.getTextureData(textureId);
console.log(`Size: ${data.width}x${data.height}`);
console.log(`Bytes: ${data.image.byteLength}`);
```

#### Notes

* Texture ID can be found in material's texture channels (baseColor, roughness, normal, etc.)
* Returns raw pixel data as ArrayBuffer
