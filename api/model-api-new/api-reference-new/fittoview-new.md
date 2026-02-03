# fitToView \[new]

#### fitToView

Fits the camera to show a specific object or the entire scene.

#### Signature

```typescript
fitToView(name?: string, duration?: number): Promise<void>
```

#### Parameters

| Name       | Type     | Required | Description                                             |
| ---------- | -------- | -------- | ------------------------------------------------------- |
| `name`     | `string` | No       | Object name to focus on. If omitted, fits entire scene. |
| `duration` | `number` | No       | Animation duration in milliseconds                      |

#### Returns

`Promise<void>` — Resolves immediately (does not wait for animation to complete).

#### Usage

```javascript
// Fit entire scene
await api.fitToView();

// Focus on specific object
await api.fitToView("Chair");

// Focus with animation
await api.fitToView("Chair", 500);
```

#### Notes

* If multiple objects share the same name, camera fits to show all of them
* Promise resolves immediately — does not wait for animation to complete
* Camera maintains its current orientation (up direction) when fitting
