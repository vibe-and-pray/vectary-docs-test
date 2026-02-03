---
hidden: true
---

# removeEventListener

You can unsubscribe to any of the [ApiEvents](../type-definitions.md#api-events) you may have subscribed previously. If a previous `callback` function used when adding the event listener is sent, it will disconnect that specific event, otherwise it disconnects all listeners created with `eventName`

```typescript
removeEventListener(
		eventName: ApiEvents,
		callback?: (result: EventResponses) => void
): Promise<void>
```

| Parameters          | Description                                                                                                                                                                                                                                                                             |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventName           | <p><a href="removeeventlistener.md#api-events">ApiEvents</a><br>Name of the event listener the method will remove.</p>                                                                                                                                                                  |
| callback (optional) | <p><code>(result:</code> <a href="removeeventlistener.md#event-responses"><code>EventResponses</code></a><code>) => void</code><br>Callback function which specifies the event you are unsubscribing to. If not used unsubscribes all listeners created with <code>eventName</code></p> |

#### Usage:&#x20;

```javascript
modelApi.removeEventListener(
		"configurator_state_change"
);
```



Example

{% embed url="https://codesandbox.io/s/add-removeeventlistener-ebeq4d?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}

&#x20;
