---
hidden: true
---

# getRotation

Returns a [Vector3](../type-definitions.md#vector3) with the rotation in 3d space of an [Object](../type-definitions.md#objects).

```typescript
getRotation(
	objectName: string
): Promise<Vector3>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr></tbody></table>



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
