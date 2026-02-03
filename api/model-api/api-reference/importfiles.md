---
hidden: true
---

# importFiles

Imports a file or an array of files to be loaded to the scene. There are multiple ways that can be used to specify the source of the files.

```typescript
importFiles(
	files: string | string[] | Blob | Blob[] | FileList
): Promise<void>
```



<table><thead><tr><th width="140">Parameters</th><th width="443">Description</th><th>Type</th></tr></thead><tbody><tr><td>files</td><td><p>Defines the source files to be imported into the current scene.</p><p>Strings can be used to fetch URLs, <a href="https://developer.mozilla.org/en-US/docs/Web/API/Blob">Blobs</a> can be used to pass down already available resources, and a <a href="https://developer.mozilla.org/en-US/docs/Web/API/FileList">FileList</a> can be used to use local resources.</p><p>These are the file extensions that work out of the gate:</p><p>.zip (containing any of the following), .jpeg, .jpg, .png, .gif, .mp4, .json, .glb, .gltf, .fbx, .obj, .stl</p></td><td><code>string</code> | <code>string[]</code> | <a href="https://developer.mozilla.org/en-US/docs/Web/API/Blob"><code>Blob</code> | <code>Blob[]</code></a> | <a href="https://developer.mozilla.org/en-US/docs/Web/API/FileList"><code>FileList</code></a></td></tr></tbody></table>



Usage:

```jsx
// String for URL, fetching happens inside the function
await modelApi.importFiles('URL');

// Blob, pre-fetched content
const blob = await fetch('URL').then(res => res.blob());
await modelApi.importFiles(blob);

// FilesList from <input type="file">
const input = document.querySelector('input[type="file"]');
input.addEventListener('change', async () => {
	await modelApi.importFiles(input.files);
}
```

