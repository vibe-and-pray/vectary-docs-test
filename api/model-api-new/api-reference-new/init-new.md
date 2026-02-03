# init \[new]

#### init



Initializes the API connection with the embedded model. Must be called before using any other API methods.



#### Signature



```typescript
init(): Promise<void>
```



#### Parameters

None.



#### Returns

`Promise<void>` — Resolves when the connection is established and the model is ready.



#### Usage



```javascript
import { VctrModelApi } from "https://app.vectary.com/studio-lite/scripts/api.js";

const api = new VctrModelApi("vectary-embed");
await api.init();

// Now you can use other API methods
const objects = await api.getObjects();
```



#### Notes



* Always `await` this method before calling other API methods
* Each iframe requires its own API instance and `init()` call
* The Promise resolves when the model has finished loading



