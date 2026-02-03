# toggleVisibility \[new]



#### toggleVisibility



Shows, hides, or toggles visibility of objects in the scene.



#### Signature

```typescript
toggleVisibility(objectNames: string[], visible?: boolean): Promise<void>
```

#### Parameters

<table><thead><tr><th width="139.5234375">Name</th><th width="115.8359375">Type</th><th width="120.5390625">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNames</code></td><td><code>string[]</code></td><td>Yes</td><td>Array of object names</td></tr><tr><td><code>visible</code></td><td><code>boolean</code></td><td>No</td><td><code>true</code> to show, <code>false</code> to hide. If omitted, toggles current state</td></tr></tbody></table>

#### Returns

`Promise<void>`

#### Usage

```javascript
// Toggle visibility (switch current state)
await api.toggleVisibility(["Chair"]);

// Hide objects
await api.toggleVisibility(["Chair", "Table"], false);

// Show objects
await api.toggleVisibility(["Chair", "Table"], true);
```

#### Notes

* When `visible` parameter is omitted, the method toggles the current visibility state
* Only accepts array of names, not a single string
