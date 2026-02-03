# setTextureData \[new]

#### setTextureData

Replaces the image data of an existing texture.

#### Signature

```typescript
setTextureData(textureId: string, image: TextureData | Blob): Promise<void>
```

#### Parameters

| Name        | Type                  | Required | Description                  |
| ----------- | --------------------- | -------- | ---------------------------- |
| `textureId` | `string`              | Yes      | ID of the texture to replace |
| `image`     | `TextureData \| Blob` | Yes      | New image data               |

```typescript
type TextureData = {
  image: ArrayBuffer;
  width: number;
  height: number;
};
```

#### Returns

`Promise<void>`

#### Usage

```javascript
// Get texture ID from material
const material = await api.getActiveMaterial("T-Shirt");
const textureId = material.baseColor.textureConfig.id;

// Replace with TextureData (from canvas)
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
ctx.drawImage(img, 0, 0);
const imgData = ctx.getImageData(0, 0, canvas.width, canvas.height);

await api.setTextureData(textureId, {
  image: imgData.data.buffer,
  width: canvas.width,
  height: canvas.height
});

// Or replace with Blob
const blob = await fetch('image.png').then(r => r.blob());
await api.setTextureData(textureId, blob);
```

#### Notes

* Replaces the texture in-place — changes are visible immediately
* Accepts both TextureData object and Blob
