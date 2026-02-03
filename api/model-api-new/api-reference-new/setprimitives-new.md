# setPrimitives \[new]

#### setPrimitives

Updates the settings of a primitive object.

#### Signature

```typescript
setPrimitives(
  name: string, 
  settings: Partial<PrimitiveNodeSettings>
): Promise<void>
```

#### Parameters

| Name       | Type                             | Required | Description                  |
| ---------- | -------------------------------- | -------- | ---------------------------- |
| `name`     | `string`                         | Yes      | Name of the primitive object |
| `settings` | `Partial<PrimitiveNodeSettings>` | Yes      | Settings to update           |

#### Returns

`Promise<void>`

#### Usage

```javascript
// Change only box dimensions (other settings preserved)
await api.setPrimitives("Box", {
  boxDimensions: { x: 2, y: 1, z: 1.5 }
});

// Change only sphere radius
await api.setPrimitives("Sphere", {
  sphereRadius: 2.5
});

// Enable rounded corners on box
await api.setPrimitives("Box", {
  roundnessEnabled: true,
  roundnessRadius: 0.2
});

// Set multiple properties
await api.setPrimitives("Box", {
  boxDimensions: { x: 1, y: 1, z: 1 },
  boxSegments: { x: 2, y: 2, z: 2 },
  roundnessEnabled: true,
  roundnessRadius: 0.1,
  roundnessRadiusSegments: 4,
  computeNormals: true
});
```

#### Notes

* Accepts `Partial<>` — only specify properties you want to change
* Unspecified properties are preserved
* Invalid properties are silently ignored
* Values can be passed as numbers (converted to strings internally)
* The object must be a primitive created in Studio
