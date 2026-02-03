# isReady \[new]



#### isReady



Returns a Promise that resolves when the API is ready to use.



#### **Signature**

```typescript
isReady(): Promise<void>
```



#### **Parameters**

None.



#### **Returns**

`Promise<void>` — Resolves when the API is ready.



#### **Usage**

```javascript
const api = new VctrModelApi("vectary-embed");
await api.isReady();

// Now you can use other API methods
```



#### **Notes**



* Works similarly to `init()` — both wait for the API to be ready
* Can be called multiple times safely
