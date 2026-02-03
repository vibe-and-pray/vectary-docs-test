---
hidden: true
---

# setViewState

Sets the current [CameraViewState](../type-definitions.md#cameraviewstate) of the scene.

```typescript
setViewState(
	viewState: CameraViewState
): Promise<void>
```



| Parameters | Description                                      | Type                                                        |
| ---------- | ------------------------------------------------ | ----------------------------------------------------------- |
| viewState  | Object describing the settings of a camera view. |   [CameraViewState](../type-definitions.md#cameraviewstate) |



Usage:

```jsx
await modelApi.setViewState({
    position: {
        x: 4000,
        y: -5500,
        z: 1250
    },
    target: {
        x: 13,
        y: -36,
        z: 495
    },
    upVector: {
        x: 0,
        y: 0,
        z: 1
    }
});
```

