---
hidden: true
---

# getText3d

Retrieves the settings of a [3DText](../../../documentation/design-process/design-mode/3d-text.md) object.

```typescript
getText3d(
	objectName: string
): Promise<Text3DNodeSettings>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what 3d text object do we want to retrieve its settings from.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```javascript
await modelApi.getText3d('3D Text');
```

Return value:

```jsx
{
    "text": "Example",
    "fontFamily": "Open Sans",
    "fontSize": 50,
    "weight": "regular",
    "distanceX": 0,
    "distanceY": 0,
    "textAlign": "CENTER",
    "textHeight": "DEFAULT",
    "curveSegments": 5,
    "contourOffset": 0
    "amount": 15,
}
```
