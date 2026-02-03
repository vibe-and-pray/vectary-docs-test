---
hidden: true
---

# raycastObject

Returns a [RayObjectHit](../type-definitions.md#rayobjecthit) of an object if intersected by the current mouse-cursor position, or the [Ray](../type-definitions.md#ray) if specified.

```typescript
raycastObject(
	objectName: string,
	ray?: Ray
): Promise<RayObjectHit | null>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>The name of the object we want to get the intersection data from.</td><td><code>string</code></td></tr><tr><td>ray (optional)</td><td>A ray specifying how we should intersect with the objects.</td><td><a href="../type-definitions.md#ray"><code>Ray</code></a></td></tr></tbody></table>



Usage:

```jsx
await modelApi.raycastObject('T-Shirt');
```



Return value:

```jsx
{
    "id": "5a9510cf-fa29-4c8b-9804-6cf6df6b43ee",
    "name": "T-Shirt",
    "position": {
        "x": 37.350260811166834,
        "y": -120.26830756045021,
        "z": 363.7658504937014
    },
    "normal": {
        "x": -0.022361778356376052,
        "y": -0.9989480768854121,
        "z": -0.03996635577118709
    },
    "uv": {
        "x": 0.20498806490294819,
        "y": 0.2775749847073309,
        "z": 0
    }
}
```
