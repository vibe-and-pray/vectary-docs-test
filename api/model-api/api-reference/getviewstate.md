---
hidden: true
---

# getViewState

Gets the current [CameraViewState](../type-definitions.md#cameraviewstate) of the scene.

```typescript
getViewState(): Promise<CameraViewState>
```



Usage:

```jsx
await modelApi.getViewState();
```



Return value:

```jsx
{
    "position": {
        "x": 3984.4911973303847,
        "y": -5567.485597975884,
        "z": 1267.920531047499
    },
    "target": {
        "x": 13.783046003519303,
        "y": -36.59329436183907,
        "z": 495.90485613717385
    },
    "upVector": {
        "x": -0.06570553967248556,
        "y": 0.09152278380316671,
        "z": 0.99363291114036
    }
}
```
