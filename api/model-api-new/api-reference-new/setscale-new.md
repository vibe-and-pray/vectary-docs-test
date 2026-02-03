# setScale \[new]

#### setScale

Sets the scale of an object.

#### Signature

```typescript
setScale(objectName: string, scale: Vector3): Promise<void>
```

#### Parameters

<table><thead><tr><th width="194.44921875">Name</th><th width="144.515625">Type</th><th width="121.58984375">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr><tr><td><code>scale</code></td><td><a href="https://help.vectary.com/api/model-api-new/api-reference-new#vector3">Vector3</a></td><td>Yes</td><td>New scale <code>{x, y, z}</code></td></tr></tbody></table>

#### Returns

`Promise<void>`

#### Usage

```javascript
// Uniform scale (2x bigger)
await api.setScale("Chair", { x: 2, y: 2, z: 2 });

// Non-uniform scale
await api.setScale("Chair", { x: 1, y: 2, z: 1 });
```

#### Notes

* **Important:** Always provide all three coordinates (x, y, z). Missing values default to `0.001`, not preserved
* Only accepts string name, not array
