---
hidden: true
---

# getPrimitives

Retrieves the settings of a [Primitive](../../../documentation/design-process/design-mode/primitives.md) object, or the [Backdrop](../../../documentation/design-process/design-mode/setup/backdrop.md) object.

```typescript
getPrimitives(
	objectName: string
): Promise<PrimitiveNodeSettings>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```javascript
await modelApi.getPrimitives('Box');
```



Return value:

```jsx
{
    "computeNormals": true,
    "boxDimensions": {
        "x": 100,
        "y": 100,
        "z": 100
    },
    "boxSegments": {
        "x": 1,
        "y": 1,
        "z": 1
    },
    "roundnessRadius": 4,
    "roundnessRadiusSegments": 4,
    "roundnessEnabled": true
}
```
