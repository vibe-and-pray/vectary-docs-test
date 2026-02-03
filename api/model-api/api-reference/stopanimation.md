---
hidden: true
---

# stopAnimation

Stops the animation specified by its name.

```typescript
stopAnimation(
	animationName: string
): Promise<void>
```



<table><thead><tr><th width="215">Parameters</th><th>Description</th><th>Type</th></tr></thead><tbody><tr><td>animationName</td><td>Name of the animation we want to stop.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```jsx
await modelApi.stopAnimation('goUp');
```

