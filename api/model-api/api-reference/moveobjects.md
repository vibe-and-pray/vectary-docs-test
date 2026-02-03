---
hidden: true
---

# moveObjects

Moves the specified objects within the scene’s hierarchy.

```tsx
moveObjects(
	objectNamesOrIds: string | string[];
	insertUnderId?: string;
	insertBeforeId?: string;
	keepGlobalPosition?: boolean;
): Promise<void}>
```

| Parameters         | Description                                                                                                                                                            | Type                   |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| objectNamesOrIds   | Name/s or id/s of the objects to duplicate.                                                                                                                            | `string` \| `string[]` |
| insertUnderId      | Specifies the group id to move the objects under.                                                                                                                      | `string`               |
| insertBeforeId     | Specifies the object id to move the objects before.                                                                                                                    | `string`               |
| keepGlobalPosition | Specifies weather or not to keep the current global transformation of the object/s to move, or to apply the matrix transform of the new parents’ (defaults to `true`). | `boolean`              |



Usage:

```jsx
*const* group = (await modelApi.getObjects('Group'))[0];            
await modelApi.moveObjects('Plant Pot', group.id, null, false);
```
