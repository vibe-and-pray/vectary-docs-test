# exportFile \[new]

### exportFile

Exports the current scene to a 3D file format. Triggers automatic download.

#### Signature

```typescript
exportFile(format: Export3DFormats, options?: ExportOptions): Promise<void>
```

#### Parameters

| Parameter | Type            | Required | Description    |
| --------- | --------------- | -------- | -------------- |
| format    | Export3DFormats | Yes      | Output format  |
| options   | ExportOptions   | No       | Export options |

```typescript
type Export3DFormats = "OBJ" | "GLTF" | "GLB" | "DAE" | "USDZ" | "FBX" | "STL";

type ExportOptions = {
  fbx?: "ASCII" | "Binary";  // Default: "ASCII"
  applyParentMatrix?: boolean;
  exportOnlyUsedUVs?: boolean;
};
```

#### Returns

`Promise<void>` — File is automatically downloaded.

#### Usage

```javascript
// Export as GLB
await api.exportFile("GLB");

// Export FBX as binary
await api.exportFile("FBX", { fbx: "Binary" });
```

#### Notes

* Triggers automatic file download in browser
* Returns `void`, not a Blob
* FBX defaults to ASCII format
