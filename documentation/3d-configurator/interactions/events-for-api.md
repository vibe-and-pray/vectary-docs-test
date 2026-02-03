# Events (for API)



### Overview

\
**Events** enable two-way communication between your embedded 3D project and your website through the Model API.

\
With Events, your website can:<br>

* **Send data to the scene** — trigger interactions, update variables, control behavior
* **Receive data from the scene** — react to user actions, track state changes<br>

Events are configured in Interactions (Interact mode):<br>

* **Event listener** trigger — receives events from your website
* **Send event** action — sends events to your website<br>

```
┌─────────────────────┐                              ┌─────────────────────┐
│                     │                              │                     │
│    Your Website     │    dispatchEvent("name")     │   Vectary Scene     │
│                     │  ──────────────────────────► │                     │
│                     │     Trigger: Event listener  │                     │
│                     │                              │                     │
│                     │    addEventListener("name")  │                     │
│                     │  ◄────────────────────────── │                     │
│                     │     Action: Send event       │                     │
│                     │                              │                     │
└─────────────────────┘                              └─────────────────────┘
```

{% hint style="warning" %}
**Event names must be unique** — duplicate names are not allowed, even across different interaction types.
{% endhint %}



### How Events Carry Values



Events and [<mark style="color:blue;">**Variables**</mark>](../variables-and-expressions/) are connected by name. Understanding this link is essential:

<table><thead><tr><th width="216.82421875">Direction</th><th>How values work</th></tr></thead><tbody><tr><td>Website → Scene</td><td>The value you send with <code>dispatchEvent("name", value)</code> is stored in a Variable called <code>name</code></td></tr><tr><td>Scene → Website</td><td>The <strong>Send event</strong> action transmits the current value of a Variable with the same name</td></tr></tbody></table>

**Example:** If you have an event called `price` and a Variable called `price` with value `99`, when the scene sends this event, your website receives `99`.

If no Variable with a matching name exists, the event sends `undefined`.



### Receiving Events from the Scene



To send data from the scene to your website:



**1. In Studio (Interact mode):**

* Create a Variable (e.g., `selected_color` with value `"red"`)
* Create an Interaction:
  * **Trigger:** On click → your object
  * **Action:** Send event → `selected_color`\
    <br>



**2. In your code:**

```javascript
api.addEventListener("selected_color", (value) => {
  console.log(value); // "red"
});
```

The event fires when the trigger condition is met (e.g., user clicks the object).



### Sending Events to the Scene



To send data from your website to the scene:



**1. In Studio (Interact mode):**



*   Create an Interaction:

    * **Trigger:** Event listener → `width`
    * **Action:** Whatever should happen (Transform, Set variable, Play animation, etc.)



**2. In your code:**



```javascript
api.dispatchEvent("width", 150);
```



The value `150` is automatically stored in a Variable called `width`, making it available in expressions.





### Debugger



The **Debugger** lets you test events directly in Studio without writing code. It simulates API calls from your website.

\
**To use the Debugger:**<br>

1. Enter Preview mode
2. Open the **Debugger** tab (appears if at least one event exists)
3. Enter a value for any event
4. Click the radio button to dispatch it

\
The Debugger also displays all Variable values and updates in real-time — useful for verifying your Interactions work correctly.



<div align="left"><figure><img src="../../../.gitbook/assets/image (236).png" alt="" width="282"><figcaption></figcaption></figure></div>



### Embed code



Once you create an event, the **Share** popup automatically generates ready-to-use code.

<div align="left"><figure><img src="../../../.gitbook/assets/image (237).png" alt="" width="374"><figcaption></figcaption></figure></div>



The generated code includes:<br>

* iframe embed with your project
* API initialization
* `addEventListener()` calls for events used in **Send event** actions
* `dispatchEvent()` calls for events used in **Event listener** triggers



```javascript
<iframe
  id="VECTARY_EMBED_ID"
  src="https://app.beta.vectary.com/p/{model_id}"
  frameborder="0"
  width="100%"
  height="480"
></iframe>

<script type="module">
  import { VctrModelApi } from "https://app.beta.vectary.com/studio-lite/scripts/api.js";
  const modelApi = new VctrModelApi("VECTARY_EMBED_ID");
  await modelApi.init();

  // Example of listening to events sent from Vectary
  modelApi.addEventListener("event_name_1", value => { 
    console.log(value);
  });

  // Example of sending an event to Vectary
	modelApi.dispatchEvent('event_name_2', 'hello');
</script>
```

{% hint style="success" %}
To update the code, synchronize the project in Share popup
{% endhint %}



For further details, refer to the [Model API docs](../../../api/model-api/).



