# getRotation \[new]

### getRotation

Returns the rotation of an object.



#### Signature

```typescript
getRotation(objectName: string): Promise<Euler>
```

#### Parameters

| Name         | Type     | Required | Description |
| ------------ | -------- | -------- | ----------- |
| `objectName` | `string` | Yes      | Object name |

#### Returns

`Promise<Euler>` — Object rotation as `{x, y, z, order}`.

* `x`, `y`, `z` — rotation angles in **degrees**
* `order` — rotation order (e.g., `"XYZ"`)

See [Euler](https://help.vectary.com/api/model-api-new/api-reference-new#euler) in Common Types.\
<br>

#### Usage

```javascript
const rotation = await api.getRotation("Chair");
console.log(rotation); // { x: 0, y: 45, z: 0, order: "XYZ" }
```

#### Notes

* Values are in **degrees**, not radians
* Returns **local** rotation (relative to parent)
* Same value as `getObjects()[0].rotation`
* Only accepts string, not array

<br>
