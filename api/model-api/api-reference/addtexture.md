---
hidden: true
---

# addTexture

Adds a new texture/image to the model, and returns its id.

```typescript
addTexture(
	image: TextureData | Blob
): Promise<string>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>image</td><td>Object containing the <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer">ArrayBuffer</a>, width and height of the texture to be set.</td><td><a href="../type-definitions.md#texturedata">TextureData</a> | <a href="https://developer.mozilla.org/en-US/docs/Web/API/Blob">Blob</a></td></tr></tbody></table>



Usage:

```jsx
// Working with Canvas and ImageData
const img = new Image();
img.onload = async () => {
	canvas.width = img.width;
	canvas.height = img.height;
	ctx.drawImage(img, 0, 0, img.width, img.height);
	const imgData = ctx.getImageData(0, 0, img.width, img.height);

	newTextureId = await modelApi.addTexture({
		image: imgData.data,
		width: imgData.width,
		height: imgData.height
	});
};
img.src = "{your_image_url}"
```

```jsx
// Working with <input type="file">
uploadButton.addEventListener('change', async (e) => {
		const blob = uploadButton.files[0];
		newTextureId = await modelApi.addTexture(blob);
	}
});
```

```jsx
// Working with URL directly
fetch("{your_image_url}")
	.then(response => response.blob())
	.then(blob => {
		newTextureId = await modelApi.addTexture(blob);
	});
```

Return value:

```jsx
"230fceca-e2cc-4011-9bf4-56c6b091ec00" // uuidv4 format
```
