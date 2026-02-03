---
hidden: true
---

# setRotation

Sets the rotation of an object base on given x, y, z values.

```typescript
setRotation(
	objectName: string,
	position: Vector3,
): Promise<void>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr><tr><td>rotation</td><td><code>x</code>, <code>y</code>, <code>z</code> Euler angles of the new rotation.</td><td><a href="../type-definitions.md#vector3"><code>Vector3</code></a></td></tr></tbody></table>



Usage:

```javascript
await modelApi.setRotation('Box', {
	x: 90, 
	y: 180, 
	z: 360
});
```

