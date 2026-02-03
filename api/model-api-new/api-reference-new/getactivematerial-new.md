# getActiveMaterial \[new]

#### getActiveMaterial

Returns the currently active material of an object.

#### Signature

```typescript
getActiveMaterial(objectName: string): Promise<Material>
```

#### Parameters

| Name         | Type     | Required | Description        |
| ------------ | -------- | -------- | ------------------ |
| `objectName` | `string` | Yes      | Name of the object |

#### Returns

`Promise<Material>` — The active material with full properties.

See [Material](https://help.vectary.com/api/model-api-new/api-reference-new#material) in Common Types.

#### Usage

```javascript
const material = await api.getActiveMaterial("Chair");
console.log(material.name);
```

#### Notes

* Only accepts string, not array
* Returns full Material object with all properties
