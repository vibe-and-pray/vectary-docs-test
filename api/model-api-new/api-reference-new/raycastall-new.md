# raycastAll \[new]

### raycastAll

Casts a ray and returns the first object hit. Uses current mouse position if no ray specified.

#### Signature

```typescript
raycastAll(ray?: Ray): Promise<RayObjectHit | null>
```

#### Parameters

<table><thead><tr><th width="106.609375">Parameter</th><th width="130.35546875">Type</th><th width="124.78515625">Required</th><th>Description</th></tr></thead><tbody><tr><td>ray</td><td>Ray</td><td>No</td><td>Custom ray to cast. If omitted, uses current mouse cursor position.</td></tr></tbody></table>

```typescript
type Ray = {
  start: Vector3;
  direction: Vector3;
};
```

#### Returns

`Promise<RayObjectHit | null>` — Hit information or `null` if no intersection.

```typescript
type RayObjectHit = {
  id: string;        // Object UUID
  name: string;      // Object name
  position: Vector3; // World position of hit point
  normal: Vector3;   // Surface normal at hit point
  uv: Vector3;       // UV coordinates (z is always 0)
};
```

#### Usage

```javascript
// Raycast from current mouse position
const hit = await api.raycastAll();
if (hit) {
  console.log("Hit object:", hit.name);
  console.log("Hit position:", hit.position);
}

// Raycast with custom ray
const ray = {
  start: { x: 0, y: -500, z: 100 },
  direction: { x: 0, y: 1, z: 0 }
};
const hit = await api.raycastAll(ray);
```

#### Notes

* Returns **first hit object only**, not an array
* Without ray parameter, uses current mouse cursor position over iframe
* Returns `null` if ray doesn't hit any object
