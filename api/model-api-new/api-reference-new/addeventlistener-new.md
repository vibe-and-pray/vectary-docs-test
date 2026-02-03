# addEventListener \[new]



#### addEventListener



Listens for events sent from the scene. Used to receive events from Interactions that have "Send event" as their action.



#### **Signature**



```typescript
addEventListener(eventName: string, callback: (value: any) => void): Promise<void>
```



#### **Parameters**

| Parameter | Type     | Required | Description                            |
| --------- | -------- | -------- | -------------------------------------- |
| eventName | string   | Yes      | Name of the event to listen for        |
| callback  | function | Yes      | Function called when event is received |



#### **Returns**



`Promise<void>`



#### **Usage**

```javascript
await api.addEventListener("product_clicked", (value) => {
  console.log("Product clicked, value:", value);
});
```



#### **How it works**<br>

1. In Studio, create an Interaction with action **Send event** and specify event name
2. The trigger can be any available Studio trigger (On click, Mouse enter, On load, etc.)
3. When triggered, your callback receives the value of a Variable with the same name as the event

If no Variable with the event name exists, the callback receives `undefined`.



#### **Notes**



* Event name must match the name specified in Studio's "Send event" action
* Multiple listeners can be added for the same event
* Use `removeEventListener()` to stop listening
