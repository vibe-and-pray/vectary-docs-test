# rotateEnvironmentMap \[new]



Rotates the HDRI environment map.

#### Signature

```typescript
rotateEnvironmentMap(degrees: number): Promise<void>
```

#### Parameters

| Parameter | Type   | Required | Description               |
| --------- | ------ | -------- | ------------------------- |
| degrees   | number | Yes      | Rotation angle in degrees |

#### Returns

`Promise<void>`

#### Usage

```javascript
// Rotate 90 degrees
await api.rotateEnvironmentMap(90);

// Rotate 180 degrees
await api.rotateEnvironmentMap(180);
```

#### Notes

* Affects the lighting and reflections in the scene
* Value is absolute rotation, not relative
