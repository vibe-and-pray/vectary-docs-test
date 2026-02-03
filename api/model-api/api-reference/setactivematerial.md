---
hidden: true
---

# setActiveMaterial

Sets the active [Material](../type-definitions.md#material) in a specific object.

```typescript
setActiveMaterial(
	objectName: string,
	materialName: string
): Promise<void>
```



| Parameters   | Description                                                   | Type     |
| ------------ | ------------------------------------------------------------- | -------- |
| objectName   | The name of the object we want to set the active Material to. | `string` |
| materialName | The name of the material we want to make active.              | `string` |



Usage:

```javascript
await modelApi.setActiveMaterial('Adjustable Headband', 'White');
```
