# setConfigurationState \[new]



#### setConfigurationState



Sets the active variants and/or materials in the scene.



#### **Signature**

```typescript
setConfigurationState(state: ConfigurationState[]): Promise<ConfigurationState[]>
```



#### **Parameters**

| Parameter | Type                  | Required | Description                                 |
| --------- | --------------------- | -------- | ------------------------------------------- |
| state     | ConfigurationState\[] | Yes      | Array of variant and material states to set |

See [ConfigurationState](https://help.vectary.com/api/model-api-new/api-reference-new#configurationstate) in Common Types.



#### **Returns**

`Promise<ConfigurationState[]>` — Array with the final configuration state after the change.



#### **Usage**

```javascript
// Switch a variant
const result = await api.setConfigurationState([
  { variant: "Chair Type", active_object: "Classic Chair" }
]);

// Switch a material
const result = await api.setConfigurationState([
  { object: "Table", active_material: "Walnut Wood" }
]);

// Switch multiple at once
const result = await api.setConfigurationState([
  { variant: "Chair Type", active_object: "Modern Chair" },
  { object: "Table", active_material: "Oak Wood" }
]);

console.log(result); // Returns updated ConfigurationState[]
```



#### **Notes**

* Triggers the `configurator_state_change` event
* You can use either names or instanceIds to identify variants, objects, and materials
* Returns the full configuration state after applying changes
