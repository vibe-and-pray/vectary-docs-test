# getPosition  \[new]

#### getPosition



Returns the position of an object.

####

#### Signature

```typescript
getPosition(objectName: string): Promise<Vector3>
```

#### Parameters

| Name         | Type     | Required | Description |
| ------------ | -------- | -------- | ----------- |
| `objectName` | `string` | Yes      | Object name |

#### Returns

`Promise<Vector3>` — Object position as `{x, y, z}`.\
\
See [Vector3](https://help.vectary.com/api/model-api-new/api-reference-new#vector3) in Common Types.

#### Usage

```javascript
const position = await api.getPosition("Chair");
console.log(position); // { x: 0, y: 100, z: 50 }
```

#### Notes

* Returns **local** coordinates (relative to parent), not world coordinates
* Coordinates use Z-up orientation
* Same value as `getObjects()[0].position`
* Only accepts string, not array
