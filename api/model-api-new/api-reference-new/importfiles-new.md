# importFiles \[new]

### importFiles

Imports files into the current scene. Supports multiple input types.

#### Signature

```typescript
importFiles(files: string | string[] | Blob | Blob[] | FileList): Promise<void>
```

#### Parameters

| Parameter | Type                                                                                                                                                                     | Required | Description            |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- | ---------------------- |
| files     | string \| string\[] \| [Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob) \| Blob\[] \| [FileList](https://developer.mozilla.org/en-US/docs/Web/API/FileList) | Yes      | Source files to import |

**Supported input types:**

* `string` — URL to fetch
* `string[]` — Multiple URLs
* `Blob` — Pre-fetched content
* `Blob[]` — Multiple blobs
* `FileList` — From `<input type="file">`

**Supported formats:** .zip, .jpeg, .jpg, .png, .gif, .mp4, .json, .glb, .gltf, .fbx, .obj, .stl

#### Returns

`Promise<void>`

#### Usage

```javascript
// From URL
await api.importFiles("https://example.com/model.glb");

// Multiple URLs
await api.importFiles([
  "https://example.com/model1.glb",
  "https://example.com/model2.glb"
]);

// From Blob (pre-fetched)
const blob = await fetch("https://example.com/model.glb").then(r => r.blob());
await api.importFiles(blob);

// From file input
const input = document.querySelector('input[type="file"]');
input.addEventListener("change", async () => {
  await api.importFiles(input.files);
});
```

#### Notes

* Imported objects are added to the scene root
* Returns `void`, not an array of imported objects
* Use `getObjects()` after import to see new objects
