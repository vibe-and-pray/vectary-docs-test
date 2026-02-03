---
hidden: true
---

# getRayFromCoordinate

Returns a [Ray](../type-definitions.md#ray) we shoot from the current camera, through pixel on canvas.

```typescript
getRayFromCoordinate(
	x: number,
	y: number,
): Promise<Ray>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>x</td><td><code>x</code> coordinate in canvas, where <code>0</code> is left, and <code>1</code> is right.</td><td><code>number</code></td></tr><tr><td>y</td><td><code>y</code> coordinate in canvas, where <code>0</code> is top and <code>1</code> is bottom.</td><td><code>number</code></td></tr></tbody></table>



Usage:

```jsx
await modelApi.getRayFromCoordinate(0.5, 0.5); // Center of canvas
```



Return value:

```jsx
{
    "start": {
        "x": 426.70406480133295,
        "y": -1117.188191256327,
        "z": 840.8804717098991
    },
    "direction": {
        "x": -0.33227362438885555,
        "y": 0.8507690937811196,
        "z": -0.4071685002579967
    }
}
```
