---
hidden: true
---

# removeMaterial

Here goes a description of what the method does

```typescript
removeMaterial(
	objectName: string,
	materialName: string
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="411">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>The name of the object we want to delete the material from.</td><td><code>string</code></td></tr><tr><td>materialName</td><td>The name of the material we want to delete from the object.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```javascript
await modelApi.removeMaterial('Adjustable Headband', 'Gold');
```
