---
hidden: true
---

# addOrEditMaterial

Adds or changes a current [Material](../type-definitions.md#material) from a specific [Object](../type-definitions.md#object). Optionally sets it as active as well.

```typescript
addOrEditMaterial(
	objectName: string,
	material: Material,
	isActive = true,
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>The name of the object we want to add/change.</td><td><code>string</code></td></tr><tr><td>material</td><td>A material object with all parameters to add/change. If a material with the same names exists, it will edit it, otherwise it will create a new one.</td><td><a href="../type-definitions.md#material"><code>Material</code></a></td></tr></tbody></table>



Usage:

```javascript
const objectName = "Adjustable Headband";

// Change Gold material
const material = await modelApi.getActiveMaterial(objectName);
material.baseColor.color.x = 255;
await modelApi.addOrEditMaterial(objectName, material);

// Add new Red material
await modelApi.addOrEditMaterial(
	objectName, 
	{
		name: 'Red',
		baseColor: {
			color: {
				x: 255
			}
		}
	},
	false
);
```
