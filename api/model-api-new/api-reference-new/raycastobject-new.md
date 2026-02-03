# raycastObject \[new]

### raycastObject

Casts a ray against a specific object. Uses current mouse position if no ray specified.

#### Signature

```typescript
raycastObject(name: string, ray?: Ray): Promise<RayObjectHit | null>
```

#### Parameters

<table><thead><tr><th width="155.421875">Parameter</th><th width="145.87890625">Type</th><th width="148.48828125">Required</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>string</td><td>Yes</td><td>Object name to test</td></tr><tr><td>ray</td><td>Ray</td><td>No</td><td>Custom ray to cast. If omitted, uses current mouse cursor position.</td></tr></tbody></table>

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
// Raycast specific object from mouse position
const hit = await api.raycastObject("Chair");
if (hit) {
  console.log("Hit at:", hit.position);
}

// Raycast with custom ray
const ray = {
  start: { x: 0, y: -500, z: 100 },
  direction: { x: 0, y: 1, z: 0 }
};
const hit = await api.raycastObject("Chair", ray);
```

#### Notes

* Tests only the specified object, ignores others
* Ray parameter is **optional** (uses mouse position if omitted)
* Returns `null` if ray doesn't hit the object
* Useful for detecting clicks on specific objects
