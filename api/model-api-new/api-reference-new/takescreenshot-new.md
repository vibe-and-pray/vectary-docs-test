# takeScreenshot \[new]

### takeScreenshot

Takes a screenshot of the current scene view.

#### Signature

```typescript
takeScreenshot(height?: number): Promise<string>
```

#### Parameters

| Parameter | Type   | Required | Description                           |
| --------- | ------ | -------- | ------------------------------------- |
| height    | number | No       | Image height in pixels. Default: 2160 |

#### Returns

`Promise<string>` — Base64 [data URL](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URLs) (`data:image/png;base64,...`)

#### Usage

```javascript
// Default size (2160px height)
const dataUrl = await api.takeScreenshot();

// Custom height (width scales proportionally)
const dataUrl = await api.takeScreenshot(1024);

// Use in image element
const img = document.createElement("img");
img.src = dataUrl;
document.body.appendChild(img);

// Download as file
const link = document.createElement("a");
link.href = dataUrl;
link.download = "screenshot.png";
link.click();

// Use with jsPDF
pdf.addImage(dataUrl, "PNG", x, y, width, height);
```

#### Notes

* Returns **data URL string**, not Blob
* Width is calculated automatically to preserve aspect ratio
* Options object `{width, height, transparent}` does **NOT** work — use simple height parameter
