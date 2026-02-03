---
hidden: true
---

# setAnimationPlayhead

Sets the playhead of an animation to a specific percentage of completion, `0 -> 100`.

```typescript
setAnimationPlayhead(
	animationName: string,
	percentage: number,
): Promise<void>
```



<table><thead><tr><th width="215">Parameters</th><th>Description</th><th>Type</th></tr></thead><tbody><tr><td>animationName</td><td>Name of the animation we want to change its playhead’s position.</td><td><code>string</code></td></tr><tr><td>percentage</td><td>Must be from <code>0</code> to <code>100</code>. Where <code>0</code> is at the beginning of the animation and <code>100</code> at the end.</td><td><code>number</code></td></tr></tbody></table>



Usage:

```jsx
await modelApi.setAnimationPlayhead('goUp', 50);
```

