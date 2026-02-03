# getHoveredObjects \[new]



#### getHoveredObjects



Returns objects currently under the cursor.



#### Signature

```typescript
getHoveredObjects(): Promise<Object[]>
```

#### Parameters

None.



#### Returns

`Promise<Object[]>` — Array of objects under the cursor with full details.\
See [Object](https://help.vectary.com/api/model-api-new/api-reference-new#object) in Common Types.

Each object includes:

* `id`, `instanceId`, `name`, `visible`, `type`
* `position`, `rotation`, `scale`
* `materials` — Array of **all** materials assigned to the object (not just the active one)
* `primitive` — Primitive-specific parameters (if applicable)
* `children` — Array of child objects

#### Usage

```javascript
const hovered = await api.getHoveredObjects();
if (hovered.length > 0) {
  console.log("Hovering over:", hovered[0].name);
  console.log("Materials:", hovered[0].materials.map(m => m.name));
}
```

#### Notes

* Returns an empty array if cursor is not over any object
* Returns full object data including all assigned materials
* Useful for implementing custom hover effects, tooltips, or material info display
