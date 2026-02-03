# getRayFromCoordinate \[new]

### getRayFromCoordinate

Converts normalized screen coordinates to a 3D ray from the camera.

#### Signature

```typescript
getRayFromCoordinate(x: number, y: number): Promise<Ray>
```

#### Parameters

<table><thead><tr><th width="120.078125">Parameter</th><th width="126.88671875">Type</th><th width="127.50390625">Required</th><th>Description</th></tr></thead><tbody><tr><td>x</td><td>number</td><td>Yes</td><td>Normalized X coordinate (0 = left, 1 = right)</td></tr><tr><td>y</td><td>number</td><td>Yes</td><td>Normalized Y coordinate (0 = top, 1 = bottom)</td></tr></tbody></table>

#### Returns

`Promise<Ray>` — Ray from camera through the screen point.

```typescript
type Ray = {
  start: Vector3;    // Ray origin (camera position)
  direction: Vector3; // Normalized direction vector
};
```

#### Usage

```javascript
// Get ray from center of canvas
const ray = await api.getRayFromCoordinate(0.5, 0.5);
console.log("Ray start:", ray.start);
console.log("Ray direction:", ray.direction);

// Get ray from click position
iframe.addEventListener("click", async (e) => {
  const rect = iframe.getBoundingClientRect();
  const x = (e.clientX - rect.left) / rect.width;
  const y = (e.clientY - rect.top) / rect.height;
  const ray = await api.getRayFromCoordinate(x, y);
  
  // Use with raycastObject
  const hit = await api.raycastObject("MyObject", ray);
});
```

#### Notes

* Coordinates are **normalized 0-1**, not pixels
* `(0, 0)` = top-left corner, `(1, 1)` = bottom-right corner
* `(0.5, 0.5)` = center of canvas
* Useful for custom click handling with `raycastObject()`
