---
hidden: true
---

# getAllMaterials

Retrieves an array of all the [Materials](../type-definitions.md#material) used in the scene.

```typescript
getAllMaterials(): Promise<Material[]>
```



Usage:

```javascript
await modelApi.getAllMaterials();
```

Return value:

```jsx
[
    {
        "id": "49b8cf58-4f73-4207-a4e9-5df743e49f4b",
        "name": "White",
        "baseColor": { ...
    },
    {
        "id": "cf551e75-c9a7-4663-9a24-da21821f00c4",
        "name": "Gold",
        "baseColor": { ...
    },
    {
        "id": "a0d895b0-ca1e-4305-b00a-495a3990bbe6",
        "name": "Plastic",
        "baseColor": { ...
    },
		{
        "id": "2fb03f36-9044-480f-ac86-6e3019e58124",
        "name": "Rubber Cable",
        "baseColor": { ...
    },
]
```
