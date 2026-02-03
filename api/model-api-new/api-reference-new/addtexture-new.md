# addTexture \[new]

#### addTexture

Adds a new texture to the scene and returns its ID.

#### Signature

```typescript
addTexture(image: TextureData | Blob | File): Promise<string>
```

#### Parameters

| Name    | Type                          | Required | Description |
| ------- | ----------------------------- | -------- | ----------- |
| `image` | `TextureData \| Blob \| File` | Yes      | Image data  |

```typescript
type TextureData = {
  image: ArrayBuffer;
  width: number;
  height: number;
};
```

#### Returns

`Promise<string>` — ID of the created texture (UUID format).

#### Usage

```javascript
// From File input
const fileInput = document.getElementById('file-input');
const textureId = await api.addTexture(fileInput.files[0]);

// From Blob (e.g., fetched image)
const blob = await fetch('image.png').then(r => r.blob());
const textureId = await api.addTexture(blob);

// From Canvas as TextureData
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
ctx.drawImage(img, 0, 0);
const imgData = ctx.getImageData(0, 0, canvas.width, canvas.height);

const textureId = await api.addTexture({
  image: imgData.data.buffer,
  width: canvas.width,
  height: canvas.height
});
```

#### Notes

* Creates texture in memory but does NOT apply it to any material
* Use `mapTextures()` to overlay on existing texture
* Use `addOrEditMaterial()` to assign to a material
* Supported formats: PNG, JPG, WebP
* URL strings are NOT supported
