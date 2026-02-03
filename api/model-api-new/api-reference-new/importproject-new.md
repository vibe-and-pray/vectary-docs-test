# importProject \[new]

### importProject

Imports another Vectary project into the current scene.

#### Signature

```typescript
importProject(projectId: string): Promise<void>
```

#### Parameters

| Parameter | Type   | Required | Description                      |
| --------- | ------ | -------- | -------------------------------- |
| projectId | string | Yes      | Project UUID from your workspace |

#### Returns

`Promise<void>`

#### Usage

```javascript
await api.importProject("bf104b1b-db6f-4a0f-89a0-624cabb1c3c7");
```

#### Notes

* Project must be **shared** (not private)
* Project ID must be in UUID format
* Get the UUID from Dashboard → Project card menu → Copy ID
* All objects from the project are imported into the current scene
* Returns `void`, not an array of imported objects
