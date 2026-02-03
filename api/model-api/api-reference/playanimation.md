---
hidden: true
---

# playAnimation

Plays the animation specified by its name.

```typescript
playAnimation(
	animationName: string
): Promise<void>
```



<table><thead><tr><th width="215">Parameters</th><th>Description</th><th>Type</th></tr></thead><tbody><tr><td>animationName</td><td>Name of the animation we want to play.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```jsx
await modelApi.playAnimation('goUp');
```
