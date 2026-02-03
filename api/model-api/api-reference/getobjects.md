---
hidden: true
---

# getObjects

Returns an array of [`Objects`](../type-definitions.md#objects) with any matches from the names or Ids inputted. If no parameter is sent, it will retrieve all objects in the scene.

```tsx
getObjects(
	objectNamesOrIds?: string[]
): Promise<Object[]}>
```

| Parameters       | Description                                                                                    | Type       |
| ---------------- | ---------------------------------------------------------------------------------------------- | ---------- |
| objectNamesOrIds | Optional array with the names or Ids of the objects you would like to retrieve from the scene. | `string[]` |



Usage:

```javascript
await modelApi.getObjects([
	"Adjustable Headband",
	"NUNO Headphones Stand",
]);
```

Return value:

```json
[
    {
        "id": "ef9d771e-9e1c-4f4a-ad2b-9a29df25ebbd",
        "name": "Adjustable Headband",
        "type": "BUFFER_OBJECT",
        "position": {
            "x": -0.07262885570526123,
            "y": 1.0778179745674117,
            "z": 32.76203308746523
        },
        "rotation": {
            "_x": 0,
            "_y": 0,
            "_z": 0,
            "_order": "XYZ"
        },
        "scale": {
            "x": 1,
            "y": 1,
            "z": 1
        },
        "materials": [
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
    },
    {
        "id": "45408cfa-a5c9-4373-9b79-bf01358a72ff",
        "name": "NUNO Headphones Stand",
        "type": "EMPTY_OBJECT",
        "position": {
            "x": 0.0000017933592815211341,
            "y": 2.4371470827027615,
            "z": -16.298621724118625
        },
        "rotation": {
            "_x": 0,
            "_y": 0,
            "_z": 0,
            "_order": "XYZ"
        },
        "scale": {
            "x": 1,
            "y": 1,
            "z": 1
        },
        "materials": []
    }
]
```
