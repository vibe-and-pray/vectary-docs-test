# duplicateObjects \[new]



#### duplicateObjects



Creates copies of objects in the scene.



#### Signature

```typescript
duplicateObjects(
  objectNamesOrIds: string | string[],
  keepName?: boolean,
  keepParent?: boolean,
  insertUnderId?: string,
  insertBeforeId?: string
): Promise<Object[]>
```

#### Parameters

<table><thead><tr><th width="173.53125">Name</th><th width="195.296875">Type</th><th width="106.92578125">Required</th><th>Description</th></tr></thead><tbody><tr><td><code>objectNamesOrIds</code></td><td><code>string | string[]</code></td><td>Yes</td><td>Object name(s) or ID(s) to duplicate</td></tr><tr><td><code>keepName</code></td><td><code>boolean</code></td><td>No</td><td>Keep original name (<code>true</code>) or append number (<code>false</code>). Default: <code>true</code></td></tr><tr><td><code>keepParent</code></td><td><code>boolean</code></td><td>No</td><td>Keep same parent (<code>true</code>) or move to root (<code>false</code>). Default: <code>false</code></td></tr><tr><td><code>insertUnderId</code></td><td><code>string</code></td><td>No</td><td>Group ID to insert duplicated objects under</td></tr><tr><td><code>insertBeforeId</code></td><td><code>string</code></td><td>No</td><td>Object ID to insert duplicated objects before</td></tr></tbody></table>

#### Returns

`Promise<Object[]>` — Array of newly created objects with full details (including `materials` and `primitive`).\
See [Object](https://help.vectary.com/api/model-api-new/api-reference-new#object) in Common Types.

#### Usage

```javascript
// Duplicate single object (string)
const copies = await api.duplicateObjects("Chair");

// Duplicate multiple objects (array)
const copies = await api.duplicateObjects(["Chair", "Table"]);

// Duplicate with numbered name
const copies = await api.duplicateObjects("Sphere", false);
// Result: "Sphere 1"

// Duplicate keeping parent hierarchy
const copies = await api.duplicateObjects("Leg", true, true);
```

#### Notes

* Duplicated objects are created at the same position as originals
* When `keepName: true` (default), all copies have the same name as the original
* When `keepName: false`, copies get numbered names (e.g., "Object 1", "Object 2")
* If multiple objects match the name, all of them are duplicated
