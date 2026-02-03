# setPosition \[new]

#### setPosition

\
Sets the position of an object.



#### Signature

```typescript
setPosition(objectName: string, position: Vector3): Promise<void>
```

#### Parameters

<table><thead><tr><th width="181.6015625">Name</th><th width="155.40625">Type</th><th width="160.15625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectName</code></td><td><code>string</code></td><td>Yes</td><td>Object name</td></tr><tr><td><code>position</code></td><td><a href="https://help.vectary.com/api/model-api-new/api-reference-new#vector3">Vector3</a></td><td>Yes</td><td>New position <code>{x, y, z}</code></td></tr></tbody></table>



#### Returns

`Promise<void>`

#### Usage

```javascript
// Set absolute position
await api.setPosition("Chair", { x: 100, y: 50, z: 0 });

// Move relative to current position
const current = await api.getPosition("Chair");
await api.setPosition("Chair", { 
  x: current.x + 10, 
  y: current.y, 
  z: current.z 
});
```

#### Notes



* Coordinates use Z-up orientation
* Sets **local** position (relative to parent)
* **Important:** Always provide all three coordinates (x, y, z). Missing values default to `0`, not current position
* Only accepts string name, not array
