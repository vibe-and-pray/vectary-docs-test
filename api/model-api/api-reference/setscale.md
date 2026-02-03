---
hidden: true
---

# setScale

Sets the scale of an object base on given x, y, z values.

```typescript
setScale(
	objectName: string,
	scale: Vector3,
): Promise<void>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr><tr><td>scale</td><td>x, y, z values of the new scale.</td><td><a href="../type-definitions.md#vector3"><code>Vector3</code></a></td></tr></tbody></table>



Usage:

```javascript
await modelApi.setScale('Box', {
	x: 1.5, 
	y: 2, 
	z: 1
});
```

