# removeObjects \[new]



#### removeObjects



Removes objects from the scene by their names or IDs.



#### Signature

```typescript
removeObjects(objectNamesOrIds: string[]): Promise<Object[]>
```

#### Parameters

| Name               | Type       | Required | Description                            |
| ------------------ | ---------- | -------- | -------------------------------------- |
| `objectNamesOrIds` | `string[]` | Yes      | Array of object names or IDs to remove |

#### Returns



`Promise<Object[]>` — Array of removed object data, including their properties at the time of removal.

Each object in the array contains:

* `id` — Object ID
* `instanceId` — Instance ID
* `name` — Object name
* `visible` — Visibility state
* `type` — Object type (e.g., `"PRIMITIVE_SPHERE"`, `"PRIMITIVE_BOX"`)
* `position` — Position `{x, y, z}`
* `rotation` — Rotation `{x, y, z, order}`
* `scale` — Scale `{x, y, z}`
* `children` — Array of child objects



#### Usage

```javascript
// Remove single object
const removed = await api.removeObjects(["Sphere"]);
console.log("Removed:", removed[0].name);

// Remove multiple objects
const removed = await api.removeObjects(["Box", "Cylinder"]);
console.log("Removed count:", removed.length);

// Remove by ID
const removed = await api.removeObjects(["8febf451-a4eb-4f3d-8c0c-369512b8595f"]);
```



#### Notes



* This action is **permanent** for the current session — removed objects cannot be restored without reloading the scene
* The method returns the full object data before removal, which can be useful for logging or undo functionality
* If an object name/ID doesn't exist, it will be silently ignored
