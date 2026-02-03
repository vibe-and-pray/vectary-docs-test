# setViewState \[new]

#### setViewState

Sets the camera position and orientation.

#### Signature

```typescript
setViewState(state: CameraViewState, duration?: number): Promise<void>
```

#### Parameters

| Name       | Type                                                                                            | Required | Description                        |
| ---------- | ----------------------------------------------------------------------------------------------- | -------- | ---------------------------------- |
| `state`    | [CameraViewState](https://help.vectary.com/api/model-api-new/api-reference-new#cameraviewstate) | Yes      | New camera state                   |
| `duration` | `number`                                                                                        | No       | Animation duration in milliseconds |

#### Returns

`Promise<void>` — Resolves immediately (does not wait for animation to complete).

#### Usage

```javascript
// Set camera instantly
await api.setViewState({
  position: { x: 500, y: -500, z: 300 },
  target: { x: 0, y: 0, z: 0 },
  upVector: { x: 0, y: 0, z: 1 }
});

// Animate camera over 1 second
await api.setViewState({
  position: { x: 500, y: -500, z: 300 },
  target: { x: 0, y: 0, z: 0 },
  upVector: { x: 0, y: 0, z: 1 }
}, 1000);

// Save and restore view
const saved = await api.getViewState();
// ... do something ...
await api.setViewState(saved, 500);
```

#### Notes

* The `upVector` is automatically normalized based on camera orientation
* Promise resolves immediately — does not wait for animation to complete
* Use `getViewState()` to save current view for later restoration
* Coordinate system is Z-up
