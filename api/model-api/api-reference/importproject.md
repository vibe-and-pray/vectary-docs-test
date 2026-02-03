---
hidden: true
---

# importProject

Imports another project from your workspace (must be shared and not private) into the current scene.

```typescript
importProject(
	projectId: string
): Promise<void>
```



<table><thead><tr><th>Parameters</th><th width="405">Description</th><th>Type</th></tr></thead><tbody><tr><td>projectId</td><td><p>The id of the project from your workspace that you would like to load into the current scene.</p><p>Must be in UUID format, which you can get from the Dashboard project card menu.<br><br><img src="../../../.gitbook/assets/image (362).png" alt=""></p></td><td><code>string</code></td></tr></tbody></table>



Usage:

```jsx
await modelApi.importProject('bf104b1b-db6f-4a0f-89a0-624cabb1c3c7');
```

