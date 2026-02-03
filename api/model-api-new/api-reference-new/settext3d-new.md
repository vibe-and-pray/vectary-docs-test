# setText3d \[new]

#### setText3d

Updates the settings of a 3D Text object.

#### Signature

```typescript
setText3d(
  name: string, 
  settings: Partial<Text3DNodeSettings>
): Promise<Text3DNodeSettings>
```

#### Parameters

| Name       | Type                          | Required | Description                |
| ---------- | ----------------------------- | -------- | -------------------------- |
| `name`     | `string`                      | Yes      | Name of the 3D Text object |
| `settings` | `Partial<Text3DNodeSettings>` | Yes      | Settings to update         |

#### Returns

`Promise<Text3DNodeSettings>` — The updated text settings.

#### Usage

```javascript
// Change text content only
await api.setText3d("3D Text", {
  text: "Hello World"
});

// Change font size only
await api.setText3d("3D Text", {
  fontSize: 80
});

// Change multiple properties
const updated = await api.setText3d("3D Text", {
  text: "Vectary",
  fontSize: 50,
  textAlign: "CENTER",
  textHeight: "UPPERCASE"
});
console.log(updated); // Full updated settings
```

#### Notes

* Accepts `Partial<>` — only specify properties you want to change
* Unspecified properties are preserved
* Returns the complete updated settings object
* Uses Google Fonts API — any `fontFamily` and `weight` combination from Google Fonts is supported
* If the provided `weight` is not found, the first available weight will be used
* The object must be a 3D Text created in Studio
