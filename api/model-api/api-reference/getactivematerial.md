---
hidden: true
---

# getActiveMaterial

Retrieves the active [Material](../type-definitions.md#material) in a specific object.

```typescript
getActiveMaterial(
	objectName: string
): Promise<Material>
```



| Parameters | Description                                                          | Type     |
| ---------- | -------------------------------------------------------------------- | -------- |
| objectName | The name of the object we want to retrieve the active Material from. | `string` |



Usage:

```javascript
await modelApi.getActiveMaterial('Adjustable Headband');
```

Return value:

```json
{
    "id": "cf551e75-c9a7-4663-9a24-da21821f00c4",
    "name": "Gold",
    "baseColor": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "color": {
            "x": 184,
            "y": 153,
            "z": 138
        }
    },
    "roughness": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 0.44
    },
    "metalness": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 1
    },
    "emission": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "color": {
            "x": 255,
            "y": 255,
            "z": 255
        },
        "value": 0
    },
    "normal": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 0
    },
    "opacity": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 1,
        "alphaMode": 0,
        "alphaCutoff": 0.5
    },
    "doubleSided": false,
    "clearcoat": {
        "amount": 0,
        "reflectivity": 0.04,
        "roughness": 0.2
    },
    "refraction": {
        "amount": 0,
        "IOR": 1.333,
        "absorptionDepth": 10,
        "absorptionColor": {
            "x": 255,
            "y": 255,
            "z": 255
        },
        "thicknessTextureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "thicknessValue": 10
    },
    "subsurface": {
        "amount": 0,
        "color": {
            "x": 255,
            "y": 255,
            "z": 255
        },
        "radius": 10
    },
    "iridescence": {
        "textureConfig": {
            "wrapping": 2,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 0
    },
    "reflectivity": {
        "textureConfig": {
            "wrapping": 0,
            "mapping": {
                "repeatX": 1,
                "repeatY": 1,
                "offsetX": 0,
                "offsetY": 0,
                "rotation": 0
            }
        },
        "value": 0.04
    },
    "baked": {
        "ambientOcclusion": {
            "textureConfig": {
                "wrapping": 0,
                "mapping": {
                    "repeatX": 1,
                    "repeatY": 1,
                    "offsetX": 0,
                    "offsetY": 0,
                    "rotation": 0
                }
            },
            "value": 0
        },
        "lightmap": {
            "textureConfig": {
                "wrapping": 0,
                "mapping": {
                    "repeatX": 1,
                    "repeatY": 1,
                    "offsetX": 0,
                    "offsetY": 0,
                    "rotation": 0
                }
            },
            "value": 1
        }
    },
    "globalMapping": {
        "offsetX": 0,
        "offsetY": 0,
        "repeatX": 1,
        "repeatY": 1,
        "rotation": 0
    }
}
```
