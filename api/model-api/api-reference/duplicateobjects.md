---
hidden: true
---

# duplicateObjects

Duplicates objects specified by name or id, names them, and places them into the scene hierarchy depending on the given options. Returns an array of the duplicated [`Objects`](../type-definitions.md#objects).

```tsx
duplicateObjects(
	objectNamesOrIds: string | string[];
	keepName?: boolean;
	keepParent?: boolean;
	insertUnderId?: string;
	insertBeforeId?: string;
): Promise<Object[]}>
```

<table><thead><tr><th width="189">Parameters</th><th width="348">Description</th><th>Type</th></tr></thead><tbody><tr><td>objectNamesOrIds</td><td>Name/s or id/s of the objects to duplicate.</td><td><code>string</code> | <code>string[]</code></td></tr><tr><td>keepName</td><td>Specifies if duplicated objects should have the same name as the original, or should append a number at the end (defaults to <code>true</code>).</td><td><code>boolean</code></td></tr><tr><td>keepParent</td><td>Specifies is duplicated objects should have the same parent as the original, or should be at the top of the scene hierarchy (defaults to <code>false</code>).</td><td><code>boolean</code></td></tr><tr><td>insertUnderId</td><td>Specifies the group id to insert the duplicated objects under.</td><td><code>string</code></td></tr><tr><td>insertBeforeId</td><td>Specifies the object id to insert the duplicated objects before.</td><td><code>string</code></td></tr></tbody></table>



Usage:

```jsx
modelApi.duplicateObjects("Sphere", false).then((copies) => {
	console.log('duplicated object/s:', copies);
}
```

Return value:

```jsx
[
    {
        "id": "5af629a1-d997-4b10-b7b6-52adcd204e7e",
        "name": "Sphere 1",
        "visible": true,
        "type": "PRIMITIVE_SPHERE",
        "position": {
            "x": 0,
            "y": 0,
            "z": 0
        },
        "rotation": {
            "x": 0,
            "y": 0,
            "z": 0,
            "order": "XYZ"
        },
        "scale": {
            "x": 1,
            "y": 1,
            "z": 1
        },
        "materials": [
            {
                "id": "1ff73858-f170-47e1-866f-34cf73784b3a",
                "name": "Cozy Vibe",
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
            "sphereRadius": 50,
            "sphereWidthSegments": 64,
            "sphereHeightSegments": 32
        },
        "children": []
    }
]
```
