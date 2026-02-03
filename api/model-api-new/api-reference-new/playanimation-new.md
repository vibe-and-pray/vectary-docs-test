# playAnimation \[new]



Plays an animation.

#### Signature

```typescript
playAnimation(name: string, options?: PlayOptions): Promise<void>
```

#### Parameters

| Parameter | Type        | Required | Description      |
| --------- | ----------- | -------- | ---------------- |
| name      | string      | Yes      | Animation name   |
| options   | PlayOptions | No       | Playback options |

```typescript
type PlayOptions = {
  loop?: boolean;
  reverse?: boolean;
};
```

#### Returns

`Promise<void>`

#### Usage

```javascript
// Play once
await api.playAnimation("Open");

// Play in loop
await api.playAnimation("Spin", { loop: true });

// Play in reverse
await api.playAnimation("Open", { reverse: true });
```
