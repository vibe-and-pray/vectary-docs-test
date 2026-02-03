---
hidden: true
---

# getScale

Returns a [Vector3](../type-definitions.md#vector3) with the scale of an [Object](../type-definitions.md#object).

```typescript
getScale(
	objectName: string
): Promise<Vector3>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```javascript
await modelApi.init();
```



Return value:

```jsx
{
	x: 1,
	y: 1,
	z: 1,
}
```
