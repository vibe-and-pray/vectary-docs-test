---
hidden: true
---

# setConfigurationState



Attempts to set an array with a [`ConfigurationState`](../type-definitions.md#configurationstate) for present [`Variants`](../../../documentation/3d-configurator/floating-ui/variants-ui.md) and [`Materials`](../../../documentation/3d-configurator/floating-ui/materials-ui.md) in the model.

Returns an array with the final [`ConfigurationState`](../type-definitions.md#configurationstate) that was set.

```typescript
setConfigurationState(
		state: Array<ConfigurationState>
): Promise<ConfigurationState[]>
```



| Parameters | Description                                                                                                                                                                                                                                                                            |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| state      | <p><code>Array&#x3C;ConfigurationState></code><br><br>An array with different states for <a href="../type-definitions.md#variantswitcherdata"><code>VariantSwitcherData</code></a> and <a href="../type-definitions.md#materialswitcherdata"><code>MaterialSwitcherData</code></a></p> |



Usage:

```javascript
await modelApi.setConfigurationState([
    {
        "variant": "Object Switcher",
        "active_object": "NUNO Stand"
    },
    {
        "object": "Adjustable Headband",
        "active_material": "White"
    }
]);
```

Return value:

```javascript
[
    {
        "switcher": "Object Switcher",
        "object": "NUNO Stand"
    },
    {
        "object": "Adjustable Headband",
        "material": "White"
    }
]
```
