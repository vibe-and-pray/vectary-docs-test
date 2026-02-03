# Type Definitions



This section contains all type definitions used within the API, offering clarity for developers implementing custom logic and integrations.



## Init



ProjectInfo

```typescript
type ProjectInfo {
	projectName: string;
	modelId: string;
	modelIdBase62: string;
	publishedId: string;
	workspaceId: string;
};
```





## EventListeners



#### Api Events

```typescript
enum ApiEvents 
	INTERACTION_CUSTOM_EVENT = "{custom_event_name}",
	MOUSE_MOVE = "mouse_move",
	MOUSE_DRAG = 'mouse_drag',
	MOUSE_DOWN = "mouse_down",
	MOUSE_UP = 'mouse_up',
	MOUSE_CLICK = "mouse_click",
	MOUSE_WHEEL = 'mouse_wheel',
	KEY_DOWN = 'key_down',
	HOVERED_OBJECT = 'hovered_object',
	CONFIGURATOR_STATE_CHANGE = "configurator_state_change",
	SELECTION_STATE_CHANGE = "configurator_state_change",
}
```



#### Event Responses

`{custom_event_name}`

Custom events need to be setup directly in studio [events-for-api.md](../../documentation/3d-configurator/interactions/events-for-api.md "mention")





`configurator_state_change`

```typescript
return ConfigurationState[]
```



## Configurators



#### ConfigurationState

```typescript
type ConfigurationState = VariantSwitcherData | MaterialSwitcherData;
```



#### VariantSwitcherData

```typescript
type VariantSwitcherData {
	variant: string;
	active_object: string;
};
```



#### MaterialSwitcherData

```typescript
type MaterialSwitcherData {
	object: string;
	active_material: string;
};
```



## Math



#### Vector3

```typescript
type Vector3 = {
	x: number;
	y: number;
	z: number;
};
```

#### Euler

```typescript
type Euler = Vector3 & {
	order?: string // default: 'XYZ'
};
```

#### Ray

```typescript
type Ray = {
	start: Vector3;
	direction: Vector3;
};
```

#### RayObjectHit

```typescript
type RayObjectHit = {
	id: string;
	name: string;
	position: Vector3;
	normal: Vector3;
	uv: Vector3;
};
```



## Objects

#### Object

```typescript
type Object = {
		id: string;
		instanceId: string;
		name: string;
		visible: boolean;
		type: sceneObjects;
		position: Vector3;
		rotation: Euler;
		scale: Vector3;
		materials?: Material[];
		primitive?: PrimitiveNodeSettings;
		text3d?: Text3DNodeSettings;
		children?: SceneObject[];
		parentId?: string;
};
```

#### SceneObjects

```typescript
enum sceneObjects {
    BUFFER_OBJECT = "BUFFER_OBJECT",

    EMPTY_OBJECT = "EMPTY_OBJECT",
    TEXT3D = "TEXT3D",
    IMAGE_PLANE = "IMAGE_PLANE",
    SVG_OBJECT = "SVG_OBJECT",

    SPOT_LIGHT = "SPOT_LIGHT",
    POINT_LIGHT = "POINT_LIGHT",
    DIRECTIONAL_LIGHT = "DIRECTIONAL_LIGHT",
    RECTANGLE_LIGHT = "RECTANGLE_LIGHT",

    CAMERA = "CAMERA",

    BEND = "BEND",
    NOISE = "NOISE",
    TAPER = "TAPER",
    TWIST = "TWIST",
    SIMPLIFY = "SIMPLIFY",
    SPHERIFY = "SPHERIFY",
    STRETCH = "STRETCH",
    SKEW = "SKEW",
    SMOOTH_NORMALS = "SMOOTH_NORMALS",

    LINEAR_CLONER = "LINEAR_ARRAY",
    RADIAL_CLONER = "RADIAL_ARRAY",
    GRID_CLONER = "GRID_ARRAY",
    OBJECT_CLONER = "OBJECT_ARRAY",
    SYMMETRY = "SYMMETRY",
    RANDOMIZE = "RANDOMIZE",

    SUBDIVISION_SURFACE = "SUBDIVISION_SURFACE",
    BEVEL = "BEVEL",

    BOOLEAN_OPERATOR = "BOOLEAN_OPERATOR",

    PRIMITIVE_BOX = "PRIMITIVE_BOX",
    PRIMITIVE_SPHERE = "PRIMITIVE_SPHERE",
    PRIMITIVE_CYLINDER = "PRIMITIVE_CYLINDER",
    PRIMITIVE_TUBE = "PRIMITIVE_TUBE",
    PRIMITIVE_CONE = "PRIMITIVE_CONE",
    PRIMITIVE_POLYHEDRON = "PRIMITIVE_POLYHEDRON",
    PRIMITIVE_TORUS = "PRIMITIVE_TORUS",
    SQUARE_PLANE = "SQUARE_PLANE",
    SHADOW_PLANE = "SHADOW_PLANE",
    INFINITE_PLANE = "INFINITE_PLANE",

    TEXTURE_BAKER = "TEXTURE_BAKER",

    OBJECT_SWITCHER = "OBJECT_SWITCHER",

    HOTSPOT = "HOTSPOT",

    NURBS_OBJECT = "NURBS_OBJECT",
}
```

### Primitives

#### PrimitiveNodeSettings

```typescript
type PrimitiveNodeSettings =
	| PrimitiveBoxSettings
	| PrimitiveConeSettings
	| PrimitiveCylinderSettings
	| PrimitivePolyhedronSettings
	| PrimitiveSphereSettings
	| PrimitiveTorusSettings
	| PrimitiveTubeSettings
	| PrimitiveCapsuleSettings
	| PrimitiveSquarePlaneSettings
	| PrimitiveCirclePlaneSettings
	| PrimitiveInfinitePlaneSettings;
```

#### PrimitiveBoxSettings

```typescript
type PrimitiveBoxSettings = {
	boxDimensions: {
		x: number;
		y: number;
		z: number;
	};
	boxSegments: {
		x: number;
		y: number;
		z: number;
	};
	roundnessEnabled: boolean;
	roundnessRadius: number;
	roundnessRadiusSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveConeSettings

```typescript
type PrimitiveConeSettings = {
	coneRadiusBottom: number;
	coneHeight: number;
	coneRadiusSegments: number;
	coneHeightSegments: number;
	coneCloseEnds: boolean;
	roundnessEnabled: boolean;
	roundnessRadius: number;
	roundnessRadiusSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveCylinderSettings

```typescript
type PrimitiveCylinderSettings = {
	cylinderRadiusTop: number;
	cylinderRadiusBottom: number;
	cylinderHeight: number;
	cylinderRadiusSegments: number;
	cylinderHeightSegments: number;
	cylinderCapSegments: number;
	cylinderCloseEnds: boolean;
	roundnessEnabled: boolean;
	roundnessRadius: number;
	roundnessRadiusSegments: number;
	computeNormals: boolean;
}
```

#### PrimitivePolyhedronSettings

```typescript
type PrimitivePolyhedronSettings = {
	polyhedronRadius: number;
	polyhedronDetail: number;
	computeNormals: boolean;
}
```

#### PrimitiveSphereSettings

```typescript
type PrimitiveSphereSettings = {
	sphereRadius: number;
	sphereWidthSegments: number;
	sphereHeightSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveTorusSettings

```typescript
type PrimitiveTorusSettings = {
	torusRingRadius: number;
	torusTubeRadius: number;
	torusTubeSegments: number;
	torusRingSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveTubeSettings

```typescript
type PrimitiveTubeSettings = {
	tubeRadiusIn: number;
	tubeRadiusOut: number;
	tubeHeight: number;
	tubeRadiusSegments: number;
	tubeHeightSegments: number;
	tubeSideSegments: number;
	roundnessEnabled: boolean;
	roundnessRadius: number;
	roundnessRadiusSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveSquarePlaneSettings

```typescript
type PrimitiveSquarePlaneSettings = {
	width: number;
	depth: number;
	widthSegments: number;
	depthSegments: number;
	cropSettings: {
		x: number;
		y: number;
		width: number;
		height: number;
	};
	roundnessEnabled: boolean;
	roundnessRadius: number;
	roundnessRadiusSegments: number;
	computeNormals: boolean;
}
```

#### PrimitiveInfinitePlaneSettings

```typescript
type PrimitiveInfinitePlaneSettings = {
	dimensions: { x: number; y: number; z: number };
	offset: number;
	angle: number;
	segments: number;
	computeNormals: boolean;
}
```

### Text3D

```typescript
export type Text3DNodeSettings = {
	text?: string;
	fontFamily?: string;
	fontSize?: number;
	weight?: string;
	distanceX?: number;
	distanceY?: number;
	textAlign?: 'LEFT' | 'CENTER' | 'RIGHT' | 'JUSTIFY';
	textHeight?: 'DEFAULT' | 'CAMELCASE' | 'UPPERCASE' | 'LOWERCASE';
	curveSegments?: number;
	contourOffset?: number;
	amount?: number;
};
```



## Materials

### Material

```typescript
type Material = {
	id?: string;
	name: string;

	baseColor?: {
		textureConfig?: TextureConfig;
		color?: Vector3;
	};
	roughness?: {
		textureConfig?: TextureConfig;
		value?: number;
	};
	metalness?: {
		textureConfig?: TextureConfig;
		value?: number;
	};
	emission?: {
		textureConfig?: TextureConfig;
		color?: Vector3;
		value?: number;
	};
	normal?: {
		textureConfig?: TextureConfig;
		value?: number;
	};
	opacity?: {
		textureConfig?: TextureConfig;
		value?: number;
		alphaMode?: AlphaMode;
		alphaCutoff?: number;
	};
	doubleSided?: boolean;
	clearcoat?: {
		amount?: number;
		reflectivity?: number;
		roughness?: number;
	};
	refraction: {
		amount?: number;
		IOR?: number;
		absorptionDepth?: number;
		absorptionColor?: Vector3;
		thicknessTextureConfig?: TextureConfig;
		thicknessValue?: number;
	};
	subsurface?: {
		amount?: number;
		color?: Vector3;
		radius?: number;
	};
	iridescence?: {
		textureConfig?: TextureConfig;
		value?: number;
	};
	reflectivity?: {
		textureConfig?: TextureConfig;
		value?: number;
	};
	baked?: {
		ambientOcclusion?: {
			textureConfig?: TextureConfig;
			value?: number;
		};
		lightmap: {
			textureConfig?: TextureConfig;
			value?: number;
		};
	};
	globalMapping?: TextureMapSettings;
};
```



<details>

<summary>AlphaMode</summary>

```typescript
enum AlphaMode {
	BLEND = 0,
	MASK = 1,
	ADDITIVE = 2,
}
```



</details>





## Textures

### TextureConfig

```typescript
type TextureConfig<T> = {
	id?: string;
	name?: string;
	filters?: TextureFilterSettings;
	mapping?: TextureMapSettings;
	wrapping?: WrapMode;
};
```



<details>

<summary>TextureFilterSettings</summary>

```typescript
type TextureFilterSettings = {
	brightness: number;
	contrast: number;
	hue: number;
	saturation: number;
	invert: boolean;
};
```

</details>

<details>

<summary>TextureMapSettings</summary>

```typescript
type TextureMapSettings = {
	offsetY: number;
	offsetX: number;
	repeatX: number;
	repeatY: number;
	rotation: number;
};
```

</details>

<details>

<summary>WrapMode</summary>

```typescript
enum WrapMode {
    REPEAT = 0,
    MIRRORED_REPEAT = 1,
    CLAMP = 2
}
```

</details>



### TextureData

```typescript
type TextureData = {
	image: ArrayBuffer;
	width: number;
	height: number;
};
```



## Cameras

### CameraSettings

```typescript
type CameraSettings = {
	cameraType?: CameraType;
	previewControls?: {
		orbitLimits?: {
			upLimit?: number;
			downLimit?: number;
			leftLimit?: number;
			rightLimit?: number;
		};
		dollyLimits?: {
			inLimit?: number;
			outLimit?: number;
		};
		panLimits?: {
			enabled?: boolean;
		};
	};
	previewTurntable?: {
		delay?: number;
		duration?: number;
		resume?: boolean;
		easing?: number;
	};
	perspective?: {
		fov?: number;
	};
	depthOfField?: {
		intensity?: number;
		depthOffset?: number;
	};
	aspectRatio?: {
		customWidth?: number;
		customHeight?: number;
	};
};
```

### CameraType

```typescript
enum CameraType {
    UNKNOWN = 0,
    PERSPECTIVE = 1,
    ORTHOGRAPHIC = 2,
}
```

### CameraViewState

```typescript
type CameraViewState = {
	target: Vector3;
	position: Vector3;
	upVector: Vector3;
};
```



## Exports

### Export3dFormats

```typescript
enum Export3DFormats {
	OBJ = 'OBJ',
	GLTF = 'GLTF',
	GLB = 'GLB',
	DAE = 'DAE',
	USDZ = 'USDZ',
	FBX = 'FBX',
	STL = 'STL',
}
```

### ExportOptions

```typescript
type ExportOptions = {
	fbx?: 'ASCII' | 'Binary';
	applyParentMatrix?: boolean;
	exportOnlyUsedUVs?: boolean;
};
```



