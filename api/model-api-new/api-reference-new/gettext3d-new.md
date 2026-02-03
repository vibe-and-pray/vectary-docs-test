# getText3d \[new]

#### getText3d

Returns the settings of a 3D Text object.

#### Signature

```typescript
getText3d(name: string): Promise<Text3DNodeSettings | null>
```

#### Parameters

| Name   | Type     | Required | Description                |
| ------ | -------- | -------- | -------------------------- |
| `name` | `string` | Yes      | Name of the 3D Text object |

#### Returns

`Promise<Text3DNodeSettings | null>` — Text settings, or `null` if object not found.

```typescript
type Text3DNodeSettings = {
  text: string;
  fontFamily: string;
  fontSize: number;
  weight: string;
  distanceX: number;
  distanceY: number;
  textAlign: 'LEFT' | 'CENTER' | 'RIGHT' | 'JUSTIFY';
  textHeight: 'DEFAULT' | 'CAMELCASE' | 'UPPERCASE' | 'LOWERCASE';
  curveSegments: number;
  amount: number;
  contourOffset: number;
};
```

#### Usage

```javascript
const settings = await api.getText3d("3D Text");
console.log(settings.text);      // "Example"
console.log(settings.fontSize);  // 50
console.log(settings.fontFamily); // "Open Sans"
```

#### Notes

* Returns `null` for non-existent objects
* Throws error for non-3D-Text objects
