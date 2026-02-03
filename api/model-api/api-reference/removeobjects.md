---
hidden: true
---

# removeObjects

Removes from the scene, and returns an array of [`Objects`](../type-definitions.md#objects) with any matches from the names or Ids inputted.&#x20;

```tsx
removeObjects(
	objectNamesOrIds: string[]
): Promise<Object[]}>
```

| Parameters       | Description                                                                         | Type       |
| ---------------- | ----------------------------------------------------------------------------------- | ---------- |
| objectNamesOrIds | array with the names or Ids of the objects you would like to remove from the scene. | `string[]` |



Usage:

```javascript
await modelApi.removeObjects([
	"Speaker Grid 2"
]);
```

Return value:

```json
[
    {
        "id": "c26eb2cf-e109-4f6d-b597-a3e289056dba",
        "instanceId": "ac250f44-2c2c-4145-bed6-599dd43d0764",
        "name": "Speaker Grid 2",
        "visible": true,
        "type": "BUFFER_OBJECT",
        "position": {
            "x": 0,
            "y": 0,
            "z": 0
        },
        "rotation": {
            "x": 0,
            "y": 0,
            "z": 0,
            "order": "XYZ"
        },
        "scale": {
            "x": 1,
            "y": 1,
            "z": 1
        },
        "children": []
    }
]
```
