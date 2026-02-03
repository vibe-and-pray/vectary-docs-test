---
hidden: true
---

# fitToView

Adjusts the current camera view to a specific object. If multiple objects share the same name, it will accommodate them all. If no objects are specified, it fits the whole scene.

```typescript
fitToView(
	objectName?: string
): Promise<void>
```



| Parameters | Description                                               | Type     |
| ---------- | --------------------------------------------------------- | -------- |
| objectName | Name of the object/s to fit into the current camera view. | `string` |



Usage:

```jsx
await modelApi.fitToView('plants');
```

