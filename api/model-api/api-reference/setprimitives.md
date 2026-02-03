---
hidden: true
---

# setPrimitives

Applies new settings to a [Primitive](../../../documentation/design-process/design-mode/primitives.md) object, or the [Backdrop](../../../documentation/design-process/design-mode/setup/backdrop.md) object.

```typescript
setPrimitives(
	objectName: string,
	primitiveSettings: PrimitiveNodeSettings
): Promise<void>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what object do we want to retrieve the information from.</td><td><code>string</code></td></tr><tr><td>primitiveSettings</td><td>New settings to be applied to the object.</td><td><a href="../type-definitions.md#primitivenodesettings">PrimitiveNodeSettings</a></td></tr></tbody></table>



Usage:

```javascript
await modelApi.setPrimitives('Box', {
    boxDimensions: {
        x: 100,
        y: 100,
        z: 200
    },
    boxSegments: {
        x: 10,
        y: 10,
        z: 20
    },
    roundnessEnabled: true,
    roundnessRadius: 8,
    roundnessRadiusSegments: 8,
    computeNormals: true
});
```

