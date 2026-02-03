# moveObjects \[new]



#### moveObjects



Moves objects within the scene hierarchy (re-parents objects).



#### Signature

```typescript
moveObjects(
  objectNamesOrIds: string | string[],
  insertUnderId?: string,
  insertBeforeId?: string,
  keepGlobalPosition?: boolean
): Promise<void>
```

#### Parameters

<table><thead><tr><th width="179.63671875">Name</th><th width="174.421875">Type</th><th width="110.39453125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNamesOrIds</code></td><td><code>string | string[]</code></td><td>Yes</td><td>Object name(s) or ID(s) to move</td></tr><tr><td><code>insertUnderId</code></td><td><code>string</code></td><td>No</td><td>Name or ID of the parent to move objects under</td></tr><tr><td><code>insertBeforeId</code></td><td><code>string</code></td><td>No</td><td>ID of the object to insert before</td></tr><tr><td><code>keepGlobalPosition</code></td><td><code>boolean</code></td><td>No</td><td>Keep world position (<code>true</code>) or apply parent's transform (<code>false</code>). Default: <code>true</code></td></tr></tbody></table>

#### Returns

`Promise<void>`

#### Usage

```javascript
// Move by name, parent by name
await api.moveObjects("Chair", "Furniture Group");

// Move by name, parent by ID
const group = (await api.getObjects("Group"))[0];
await api.moveObjects("Chair", group.id);

// Move multiple objects
await api.moveObjects(["Chair", "Table"], group.id);

// Move and apply parent's transform
await api.moveObjects("Wheel", carId, null, false);
```

#### Notes

* This changes the hierarchy (parent-child relationship), not the world position by default
* When `keepGlobalPosition: true` (default), objects stay in the same world position
* When `keepGlobalPosition: false`, objects inherit the parent's transformation
* Use `setPosition()` to change object position in 3D space
* Cannot move an object under itself
