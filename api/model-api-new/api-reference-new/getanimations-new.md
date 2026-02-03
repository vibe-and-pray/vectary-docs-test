# getAnimations \[new]



Returns a list of all animations in the scene.

#### Signature

```typescript
getAnimations(): Promise<string[]>
```

#### Parameters

None.

#### Returns

`Promise<string[]>` — Array of animation names.

#### Usage

```javascript
const animations = await api.getAnimations();
console.log(animations); // ["Open", "Close", "Spin"]
```
