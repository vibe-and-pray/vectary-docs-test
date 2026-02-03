---
hidden: true
---

# addEventListener

You can subscribe to any of the [`ApiEvents`](addeventlistener.md#api-events), by adding a callback function that will execute whenever the subscribed event triggers.

```typescript
addEventListener(
		eventName: ApiEvents, 
		callback: (result: EventResponses) => void
): Promise<void>
```

<table><thead><tr><th width="266">Parameters</th><th>Description</th></tr></thead><tbody><tr><td>eventName</td><td><a href="addeventlistener.md#api-events">ApiEvents</a><br>Name of the event that the method will subscribe to.</td></tr><tr><td>callback</td><td><code>(result:</code> <a href="addeventlistener.md#event-responses"><code>EventResponses</code></a><code>) => void</code><br>Callback function which takes as parameter the result of the event you are subscribing to.</td></tr></tbody></table>

#### Usage:

```javascript
modelApi.addEventListener(
		"configurator_state_change",
		(res) => {
		    // Your code here
		}
);
```



Example&#x20;

{% embed url="https://codesandbox.io/s/add-removeeventlistener-ebeq4d?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}

