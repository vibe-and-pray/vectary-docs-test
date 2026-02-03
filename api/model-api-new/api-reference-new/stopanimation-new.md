# stopAnimation \[new]



Stops a playing animation.

#### Signature

```typescript
stopAnimation(name: string): Promise<void>
```

#### Parameters

| Parameter | Type   | Required | Description    |
| --------- | ------ | -------- | -------------- |
| name      | string | Yes      | Animation name |

#### Returns

`Promise<void>`

#### Usage

```javascript
await api.stopAnimation("Spin");
```
