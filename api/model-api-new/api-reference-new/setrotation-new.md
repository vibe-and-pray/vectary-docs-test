# setRotation \[new]

#### setRotation

Sets the rotation of an object.



#### Signature

```typescript
setRotation(objectName: string, rotation: Euler): Promise<void>
```



#### Parameters

<table><thead><tr><th width="166.328125">Name</th><th width="136.90625">Type</th><th width="115.171875">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr><tr><td><code>rotation</code></td><td><a href="https://help.vectary.com/api/model-api-new/api-reference-new#euler">Euler</a></td><td>Yes</td><td>New rotation <code>{x, y, z}</code> in degrees. Optional <code>order</code> field.</td></tr></tbody></table>

#### Returns

`Promise<void>`

#### Usage

```javascript
// Rotate 45 degrees around Y axis
await api.setRotation("Chair", { x: 0, y: 45, z: 0 });

// With explicit rotation order
await api.setRotation("Chair", { x: 90, y: 0, z: 0, order: "XYZ" });
```

#### Notes

* Values are in **degrees**, not radians
* Sets **local** rotation (relative to parent)
* **Important:** Always provide all three coordinates (x, y, z). Missing values become `null`, not preserved
* The `order` field is optional (defaults to "XYZ")
* Only accepts string name, not array









