---
hidden: true
---

# toggleVisibility

Toggles/changes the visibility of the [`Objects`](../type-definitions.md#objects) specified. You can use an optional parameter to force the visibility of the objects instead of toggling.

```tsx
toggleVisibility(
	objectNames: string[],
	visible?: boolean
): Promise<void>
```

| Parameters  | Description                                                                     | Type       |
| ----------- | ------------------------------------------------------------------------------- | ---------- |
| objectNames | Array of the names of the objects you would like to toggle the visibility from. | `string[]` |
| visible     | Optional boolean to force/specify the visibility                                | `boolean`  |
|             |                                                                                 |            |

Usage:

```javascript
await modelApi.toggleVisibility(["Box"]);
```

