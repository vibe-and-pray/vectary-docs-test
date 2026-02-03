---
hidden: true
---

# getMaterials

Retrieves an array of all the [Materials](../type-definitions.md#material) in a specific object.

```typescript
getMaterials(
	objectName: string
): Promise<Material[]>
```



| Parameters | Description                                                          | Type     |
| ---------- | -------------------------------------------------------------------- | -------- |
| objectName | Specifies what object do we want to retrieve the Material list from. | `string` |



Usage:

```javascript
await modelApi.getMaterials('Adjustable Headband');
```

Return value:

```json
[
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
    },
    {
        "id": "49b8cf58-4f73-4207-a4e9-5df743e49f4b",
        "name": "White",
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
                "x": 239,
                "y": 239,
                "z": 239
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
            "value": 0.59
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
            "value": 0
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
]
```
