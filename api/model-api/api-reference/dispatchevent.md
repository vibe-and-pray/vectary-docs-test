---
hidden: true
---

# dispatchEvent

You can send [Interaction’s Custom Events](../../../documentation/3d-configurator/interactions/events-for-api.md) with a value to the Model to trigger interactions and affect their conditions.



<pre class="language-typescript"><code class="lang-typescript"><strong>dispatchEvent (
</strong>	eventName: string
	value?: number | string | boolean | void
): Promise&#x3C;void>
</code></pre>

| Parameters       | Description                                                                                                      | Type                                  |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| eventName        | <p><a href="dispatchevent.md#api-events">ApiEvents</a><br>Name of the event listener the method will remove.</p> |                                       |
| value (optional) | Value you want to send along.                                                                                    | `number \| string \| boolean \| void` |



#### Usage&#x20;

```javascript
await modelApi.dispatchEvent("temperature", 26);
```



Examples&#x20;



{% embed url="https://codesandbox.io/p/sandbox/dispatchevent-xgk5gd" fullWidth="true" %}

{% embed url="https://codesandbox.io/s/dispatchevent-f323xt?autoresize=1&expanddevtools=1&fontsize=14&hidenavigation=1&theme=dark&codemirror=1" fullWidth="true" %}

