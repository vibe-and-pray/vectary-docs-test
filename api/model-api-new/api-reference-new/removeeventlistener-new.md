# removeEventListener  \[new]



#### removeEventListener



Removes a previously registered event listener.

<br>

#### **Signature**

```typescript
removeEventListener(eventName: string, callback?: (value: any) => void): Promise<void>
```



#### **Parameters**

| Parameter | Type     | Required | Description                                                                                 |
| --------- | -------- | -------- | ------------------------------------------------------------------------------------------- |
| eventName | string   | Yes      | Name of the event                                                                           |
| callback  | function | No       | The callback function to remove. If not provided, removes all listeners for this event name |



#### **Returns**

`Promise<void>`



#### **Usage**

```javascript
// Define callback as a named function
const handleClick = (value) => {
  console.log("Clicked:", value);
};

// Add listener
await api.addEventListener("product_clicked", handleClick);

// Remove specific listener
await api.removeEventListener("product_clicked", handleClick);

// Or remove ALL listeners for this event
await api.removeEventListener("product_clicked");
```



#### **Notes**



* To remove a specific listener, pass the exact same function reference used in `addEventListener()`
* Anonymous functions cannot be removed individually — store the function in a variable first
* Call without callback to remove all listeners for the given event name<br>
