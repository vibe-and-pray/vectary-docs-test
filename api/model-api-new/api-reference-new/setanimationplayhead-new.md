# setAnimationPlayhead  \[new]



Sets the animation progress to a specific position.

#### Signature

```typescript
setAnimationPlayhead(name: string, value: number): Promise<void>
```

#### Parameters

| Parameter | Type   | Required | Description            |
| --------- | ------ | -------- | ---------------------- |
| name      | string | Yes      | Animation name         |
| value     | number | Yes      | Progress value (0-100) |

#### Returns

`Promise<void>`

#### Usage

```javascript
// Go to start
await api.setAnimationPlayhead("Open", 0);

// Go to middle
await api.setAnimationPlayhead("Open", 50);

// Go to end
await api.setAnimationPlayhead("Open", 100);
```

#### Notes

* Value is a percentage from 0 to 100
* The animation is paused at the specified position
