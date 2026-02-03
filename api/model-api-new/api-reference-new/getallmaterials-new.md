# getAllMaterials \[new]

#### getAllMaterials

Returns all materials in the scene.

#### Signature

```typescript
getAllMaterials(): Promise<Material[]>
```

#### Parameters

None.

#### Returns

`Promise<Material[]>` — Array of all materials in the scene.

See [Material](https://help.vectary.com/api/model-api-new/api-reference-new#material) in Common Types.

#### Usage

```javascript
const materials = await api.getAllMaterials();
console.log(materials.map(m => m.name));
```

#### Notes

* Returns all materials, including those not assigned to any object
* Each material includes full properties (baseColor, roughness, metalness, etc.)
