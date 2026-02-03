---
hidden: true
---

# getPosition

Returns a [Vector3](../type-definitions.md#vector3) with the position in 3d space of an [Object](../type-definitions.md#objects).

```typescript
getPosition(
	objectName: string
): Promise<Vector3>
```

| Parameters | Description                                                        | Type     |
| ---------- | ------------------------------------------------------------------ | -------- |
| objectName | Specifies what object do we want to retrieve the information from. | `string` |



Usage:

```javascript
await modelApi.getPosition("Box");
```



Return value:

```jsx
{
	x: 0,
	y: 0,
	z: 0,
}
```
