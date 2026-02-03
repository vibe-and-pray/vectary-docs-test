# setActiveMaterial \[new]

#### setActiveMaterial

Sets the active material of an object.

#### Signature

```typescript
setActiveMaterial(objectName: string, materialName: string): Promise<void>
```

#### Parameters

| Name           | Type     | Required | Description                      |
| -------------- | -------- | -------- | -------------------------------- |
| `objectName`   | `string` | Yes      | Name of the object               |
| `materialName` | `string` | Yes      | Name of the material to activate |

#### Returns

`Promise<void>`

#### Usage

```javascript
await api.setActiveMaterial("Chair", "Leather Red");
```

#### Notes

* The material must already be assigned to the object
* Does NOT trigger the `configurator_state_change` event
* Use `setConfigurationState()` if you need the event to fire
