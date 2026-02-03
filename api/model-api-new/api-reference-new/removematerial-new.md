# removeMaterial \[new]

#### removeMaterial

Removes a material from an object.

#### Signature

```typescript
removeMaterial(objectName: string, materialName: string): Promise<void>
```

#### Parameters

| Name           | Type     | Required | Description                    |
| -------------- | -------- | -------- | ------------------------------ |
| `objectName`   | `string` | Yes      | Name of the object             |
| `materialName` | `string` | Yes      | Name of the material to remove |

#### Returns

`Promise<void>`

#### Usage

```javascript
await api.removeMaterial("Chair", "Old Material");
```

#### Notes

* Cannot remove the last material from an object
* The material is only removed from this object, not deleted from the scene
