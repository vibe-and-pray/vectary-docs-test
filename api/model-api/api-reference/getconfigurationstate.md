---
hidden: true
---

# getConfigurationState

Returns an array with the current [`ConfigurationState`](../type-definitions.md#configurationstate) of all [`Variants`](../../../documentation/3d-configurator/floating-ui/variants-ui.md) and [`Materials`](../../../documentation/3d-configurator/floating-ui/materials-ui.md)&#x20;

```tsx
getConfigurationState(): Promise<ConfigurationState[]>
```

***

Usage:

```typescript
await modelApi.getConfigurationState();
```

Return value:

```javascript
[
    [
        {
            "variant": "Object Switcher",
            "active_object": "NUNO Stand"
        },
        {
            "object": "Adjustable Headband",
            "active_material": "White"
        }
    ]
]
```
