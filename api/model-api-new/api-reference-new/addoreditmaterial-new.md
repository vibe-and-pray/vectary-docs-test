# addOrEditMaterial \[new]

#### addOrEditMaterial

Adds a new material to an object or edits an existing one.

#### Signature

```typescript
addOrEditMaterial(
  objectName: string, 
  material: Material, 
  isActive?: boolean
): Promise<Material>
```

#### Parameters

| Name         | Type       | Required | Description                                        |
| ------------ | ---------- | -------- | -------------------------------------------------- |
| `objectName` | `string`   | Yes      | Name of the object                                 |
| `material`   | `Material` | Yes      | Material properties (must include `name`)          |
| `isActive`   | `boolean`  | No       | Whether to set as active material. Default: `true` |

See [Material](https://help.vectary.com/api/model-api-new/api-reference-new#material) in Common Types.

#### Returns

`Promise<Material>` — The created or updated material with all properties.

#### Usage

```javascript
// Add new material (becomes active by default)
const mat = await api.addOrEditMaterial("Chair", {
  name: "Custom Red",
  baseColor: { color: { x: 255, y: 0, z: 0 } }
});

// Add material but don't make it active
await api.addOrEditMaterial("Chair", {
  name: "Custom Blue",
  baseColor: { color: { x: 0, y: 0, z: 255 } }
}, false);

// Edit existing material
await api.addOrEditMaterial("Chair", {
  name: "Custom Red",  // same name = edit
  roughness: { value: 0.8 }
});
```

#### Notes

* If a material with the same `name` exists on the object, it will be updated
* If the material doesn't exist, it will be created and assigned
* By default (`isActive=true`), the new/edited material becomes active
* Use `isActive: false` to add without changing the active material
* Color values use RGB in range 0-255
