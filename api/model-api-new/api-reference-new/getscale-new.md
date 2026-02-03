# getScale \[new]

#### getScale

Returns the scale of an object.

#### Signature

```typescript
getScale(objectName: string): Promise<Vector3>
```

#### Parameters

| Name         | Type     | Required | Description |
| ------------ | -------- | -------- | ----------- |
| `objectName` | `string` | Yes      | Object name |

#### Returns

`Promise<Vector3>` — Object scale as `{x, y, z}`.\
See [Vector3](https://help.vectary.com/api/model-api-new/api-reference-new#vector3) in Common Types.<br>

#### Usage

```javascript
const scale = await api.getScale("Chair");
console.log(scale); // { x: 1, y: 1, z: 1 }
```

#### Notes

* Default scale is `{ x: 1, y: 1, z: 1 }`
* Returns **local** scale (relative to parent)
* Only accepts string, not array
