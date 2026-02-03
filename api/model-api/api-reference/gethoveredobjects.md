---
hidden: true
---

# getHoveredObjects

Returns an array of [`Objects`](../type-definitions.md#objects) that are intersecting with the cursor.

```typescript
getHoveredObjects(): Promise<Object[]>
```

***

Usage:

```javascript
modelApi.addEventListener('mouse_click', async () => {
	const objects = await modelApi.getHoveredObjects();
	if (objects.length) {
		const object = objects[0];
		console.log(object);
	}
});
```

Return value:

```javascript
{
    "id": "938fafa7-f9d8-4b23-9d6a-1d2d6d0fb73d",
    "name": "Box",
    "type": "PRIMITIVE_BOX",
    "position": {
        "x": -100,
        "y": 100,
        "z": 0
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
            "id": "2e337e8e-b669-4221-a0ca-32f7978c45ab",
            "name": "Bronco",
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
                "value": 0.2
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
    ],
    "primitive": {
        "computeNormals": true,
        "boxDimensions": {
            "x": 100,
            "y": 100,
            "z": 100
        },
        "boxSegments": {
            "x": 1,
            "y": 1,
            "z": 1
        },
        "roundnessRadius": 4,
        "roundnessRadiusSegments": 4,
        "roundnessEnabled": true
    },
    "children": []
}
```
