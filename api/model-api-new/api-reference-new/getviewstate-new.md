# getViewState \[new]

#### getViewState

Returns the current camera position and orientation.

#### Signature

```typescript
getViewState(): Promise<CameraViewState>
```

#### Parameters

None.

#### Returns

`Promise<CameraViewState>` — Current camera state. \
See [CameraViewState](https://help.vectary.com/api/model-api-new/api-reference-new#cameraviewstate) in Common Types.

#### Usage

```javascript
const view = await api.getViewState();
console.log("Camera position:", view.position);
console.log("Looking at:", view.target);
console.log("Up direction:", view.upVector);

// Save for later restore
const savedView = await api.getViewState();
```

#### Notes

* `position` — camera location in world coordinates
* `target` — point the camera is looking at
* `upVector` — camera's "up" direction (typically close to Z-up)
* All values are numbers
