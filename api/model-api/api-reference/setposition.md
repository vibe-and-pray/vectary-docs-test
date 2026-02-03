---
hidden: true
---

# setPosition

Sets the position of an object base on given x, y, z values.

```typescript
setPosition(
	objectName: string,
	position: Vector3,
): Promise<void>
```

| Parameters | Description                                                        | Type                                        |
| ---------- | ------------------------------------------------------------------ | ------------------------------------------- |
| objectName | Specifies what object do we want to retrieve the information from. | `string`                                    |
| position   | `x`, `y`, `z` coordinates of the new position.                     | [`Vector3`](../type-definitions.md#vector3) |



Usage:

```javascript
await modelApi.setPosition('Box', {
	x: 100, 
	y: 100, 
	z: 0
});
```

