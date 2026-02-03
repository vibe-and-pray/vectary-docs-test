# getObjects \[new]



#### getObjects



Returns objects from the scene by name or ID, or all objects if no parameter is specified.



#### **Signature**

```typescript
getObjects(objectNamesOrIds?: string | string[]): Promise<Object[]>
```



#### **Parameters**

| Parameter        | Type                | Required | Description                                                            |
| ---------------- | ------------------- | -------- | ---------------------------------------------------------------------- |
| objectNamesOrIds | string \| string\[] | No       | Object name/ID or array of names/IDs. If omitted, returns all objects. |

#### **Returns**

`Promise<Object[]>` — Array of matching objects.

See [Object](https://help.vectary.com/api/model-api-new/api-reference-new#object) in Common Types.



#### **Usage**

```javascript
// Get all objects
const allObjects = await api.getObjects();

// Get single object by name
const sphere = await api.getObjects("Sphere");

// Get multiple objects by names
const objects = await api.getObjects(["Sphere", "Box"]);
```



#### **Notes**

* Wildcard `"*"` does NOT work — returns empty array
* Both string and array parameters are accepted
* Returns empty array if no objects match
