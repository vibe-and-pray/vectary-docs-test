# dispatchEvent  \[new]



#### dispatchEvent



Sends an event to the scene. Used to trigger Interactions that have "Event listener" as their trigger.



#### **Signature**

```typescript
dispatchEvent(eventName: string, value?: any): Promise<void>
```



#### **Parameters**

| Parameter | Type   | Required | Description                   |
| --------- | ------ | -------- | ----------------------------- |
| eventName | string | Yes      | Name of the event to dispatch |
| value     | any    | No       | Value to send with the event  |

#### **Returns**

`Promise<void>`



#### **Usage**

```javascript
// Send event without value
await api.dispatchEvent("reset");

// Send event with number
await api.dispatchEvent("width", 150);

// Send event with string
await api.dispatchEvent("color", "red");
```



#### **How it works**



1. Call `dispatchEvent()` from your website
2. In Studio, an Interaction with trigger **Event listener** and matching event name receives it
3. The Interaction executes its action (Transform, Set variable, Play animation, etc.)

If a Variable with the same name exists, its value is updated with the sent value.



#### **Supported value types**

| Type                 | Example          | Received as                   |
| -------------------- | ---------------- | ----------------------------- |
| Number               | `42`, `3.14`     | ✅ number                      |
| String               | `"hello"`        | ✅ string                      |
| Boolean              | `true`, `false`  | ✅ boolean                     |
| Array                | `[255, 128, 0]`  | ⚠️ First element only (`255`) |
| Object               | `{r: 255, g: 0}` | ⚠️ First value only (`255`)   |
| null                 | `null`           | ⚠️ Becomes `0`                |
| undefined / no value | `undefined`      | ⚠️ Becomes `0`                |

**Notes**

* Event name must match the name in Studio's Event listener trigger
* If no Variable with the event name exists, the value is not stored (but the event still triggers)
* For complex data, consider sending individual values or JSON-encoded strings
