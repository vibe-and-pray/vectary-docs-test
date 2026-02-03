---
hidden: true
---

# setText3d

Sets new settings for a [`3DText`](../../../documentation/design-process/design-mode/3d-text.md) object. We are using the [Google Fonts API](https://developers.google.com/fonts/docs/developer_api), so you can use any combination of `fontFamily` and `weight` from that service. If the provided `weight` option is not found, the first option available will be used.

Make sure to check the [get-setText3d](https://codesandbox.io/p/sandbox/get-settext3d-nvmzqq) sandbox for a working example.

```typescript
setText3d(
	objectName: string,
	settings: Text3DNodeSettings
): Promise<Text3DNodeSettings>
```

<table><thead><tr><th>Parameters</th><th width="318">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectName</td><td>Specifies what 3d text object do we want to retrieve its settings from.</td><td><code>string</code></td></tr><tr><td>settings</td><td>New settings that will be applied to the 3D Text object.</td><td><a href="../type-definitions.md#text3d"><code>Text3DNodeSetting</code></a></td></tr></tbody></table>



Usage:

```javascript
await modelApi.getText3d('3D Text', {
	fontFamily: "Roboto",
	weight: "100"
});
```

Return value:

```jsx
{
    "text": "Example",
    "fontFamily": "Roboto",
    "fontSize": 50,
    "weight": "100",
    "distanceX": 0,
    "distanceY": 0,
    "textAlign": "CENTER",
    "textHeight": "DEFAULT",
    "curveSegments": 5,
    "contourOffset": 0
    "amount": 15,
}
```
