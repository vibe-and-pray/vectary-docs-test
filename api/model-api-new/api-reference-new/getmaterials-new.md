# getMaterials \[new]

#### getMaterials

Returns materials assigned to a specific object.

#### Signature

```typescript
getMaterials(objectName: string): Promise<Material[]>
```

#### Parameters

| Name         | Type     | Required | Description        |
| ------------ | -------- | -------- | ------------------ |
| `objectName` | `string` | Yes      | Name of the object |

#### Returns

`Promise<Material[]>` — Array of materials assigned to the object.

See [Material](https://help.vectary.com/api/model-api-new/api-reference-new#material) in Common Types.

#### Usage

```javascript
const materials = await api.getMaterials("Chair");
console.log(materials.map(m => m.name));
```

#### Notes

* Only accepts string, not array
* An object can have multiple materials assigned
* Only one material is active at a time
