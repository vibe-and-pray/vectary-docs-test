---
hidden: true
---

# takeScreenshot

This method generates a screenshot(image/png) of the current camera view with a height of 2160px, or you can specify your own, while preserving the aspect ratio of the current canvas. The return data is the [url from the generated image](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URLs).

```typescript
takeScreenshot(
	height?: number
): Promise<string>
```



| Parameters | Description                               | Type     |
| ---------- | ----------------------------------------- | -------- |
| height     | The height which the screenshot will have | `number` |



Usage:

```jsx
await modelApi.takeScreenshot(1024);
```



Return value:

```jsx
"data:image/png;base64,<data>"
```

{% embed url="https://codesandbox.io/s/takescreenshot-pgy6gf?autoresize=1&expanddevtools=0&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}
