---
description: Complete list of Model API methods organized by category.
---

# API Reference \[new]



New methods and features are added to the API over time. While we aim to keep this reference up to date, some methods may not yet be documented or may lack complete details.

We welcome your questions and feedback. If something is unclear, missing, incorrect, or not working as described, please [contact us](https://www.vectary.com/contact/).





## Methods



### Initialization

<table><thead><tr><th width="45.98046875">#</th><th width="113.5">Method</th><th width="431.625">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>1</td><td><a href="init-new.md"><mark style="color:blue;"><strong>init</strong></mark></a></td><td>Initialize API connection with the embedded model</td><td><a href="https://codesandbox.io/s/init-00jr7l">Init</a></td></tr><tr><td>2</td><td><a href="isready-new.md"><mark style="color:blue;"><strong>isReady</strong></mark></a></td><td>Check if the API is ready</td><td><a href="https://codesandbox.io/s/init-00jr7l">Init</a></td></tr><tr><td>3</td><td><a href="projectinfo-new.md"><mark style="color:blue;"><strong>projectInfo</strong></mark></a></td><td>Get project information</td><td><a href="https://codesandbox.io/s/init-00jr7l">Init</a></td></tr></tbody></table>

***



### Events

<table><thead><tr><th width="45.1640625">#</th><th width="197.1953125">Method</th><th width="278.3515625">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>4</td><td><a href="dispatchevent-new.md"><mark style="color:blue;"><strong>dispatchEvent</strong></mark></a></td><td>Send event to the scene</td><td><a href="https://codesandbox.io/p/sandbox/dispatchevent-f323xt">dispatchEvent</a></td></tr><tr><td>5</td><td><a href="addeventlistener-new.md"><mark style="color:blue;"><strong>addEventListener</strong></mark></a></td><td>Listen for events from the scene</td><td><a href="https://codesandbox.io/s/add-removeeventlistener-ebeq4d">add-removeEventListener</a></td></tr><tr><td>6</td><td><a href="removeeventlistener-new.md"><mark style="color:blue;"><strong>removeEventListener</strong></mark></a></td><td>Remove event listener</td><td><a href="https://codesandbox.io/s/add-removeeventlistener-ebeq4d">add-removeEventListener</a></td></tr></tbody></table>

***



### Configuration

<table><thead><tr><th width="43.25">#</th><th width="199.7890625">Method</th><th width="274.7734375">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>7</td><td><a href="getconfigurationstate-new.md"><mark style="color:blue;"><strong>getConfigurationState</strong></mark></a></td><td>Get current variants and materials state</td><td><a href="https://codesandbox.io/s/get-setconfigurationstate-kl0psw">get-setConfigurationState</a></td></tr><tr><td>8</td><td><a href="setconfigurationstate-new.md"><mark style="color:blue;"><strong>setConfigurationState</strong></mark></a></td><td>Set variants and materials state</td><td><a href="https://codesandbox.io/s/get-setconfigurationstate-kl0psw">get-setConfigurationState</a></td></tr></tbody></table>

***



### Objects

<table><thead><tr><th width="49.75">#</th><th width="186.04296875">Method</th><th width="301.296875">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>9</td><td><a href="getobjects-new.md"><mark style="color:blue;"><strong>getObjects</strong></mark></a></td><td>Get objects by name or all objects</td><td><a href="https://codesandbox.io/p/sandbox/getobjects-thf9hc">getObjects</a></td></tr><tr><td>10</td><td><a href="removeobjects-new.md"><mark style="color:blue;"><strong>removeObjects</strong></mark></a></td><td>Remove objects from the scene</td><td><a href="https://codesandbox.io/p/devbox/getobjects-forked-dy7k3x">removeObjects</a></td></tr><tr><td>11</td><td><a href="gethoveredobjects-new.md"><mark style="color:blue;"><strong>getHoveredObjects</strong></mark></a></td><td>Get objects currently under cursor</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>12</td><td><a href="duplicateobjects-new.md"><mark style="color:blue;"><strong>duplicateObjects</strong></mark></a></td><td>Duplicate objects</td><td><a href="https://codesandbox.io/p/sandbox/duplicateobjects-rh2fh9">duplicateObjects</a></td></tr><tr><td>13</td><td><a href="moveobjects-new.md"><mark style="color:blue;"><strong>moveObjects</strong></mark></a></td><td>Move objects in hierarchy</td><td><a href="https://codesandbox.io/p/sandbox/moveobjects-7ynjmq">moveObjects</a></td></tr><tr><td>14</td><td><a href="togglevisibility-new.md"><mark style="color:blue;"><strong>toggleVisibility</strong></mark></a></td><td>Show or hide objects</td><td><a href="https://codesandbox.io/p/sandbox/togglevisibility-2r9fcw">toggleVisibility</a></td></tr></tbody></table>

***



### Transformations

<table><thead><tr><th width="51.30078125">#</th><th width="173.01953125">Method</th><th width="328.69140625">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>15</td><td><a href="getposition-new.md"><mark style="color:blue;"><strong>getPosition</strong></mark></a></td><td>Get object position</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>16</td><td><a href="setposition-new.md"><mark style="color:blue;"><strong>setPosition</strong></mark></a></td><td>Set object position</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>17</td><td><a href="getrotation-new.md"><mark style="color:blue;"><strong>getRotation</strong></mark></a></td><td>Get object rotation</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>18</td><td><a href="setrotation-new.md"><mark style="color:blue;"><strong>setRotation</strong></mark></a></td><td>Set object rotation</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>19</td><td><a href="getscale-new.md"><mark style="color:blue;"><strong>getScale</strong></mark></a></td><td>Get object scale</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr><tr><td>20</td><td><a href="setscale-new.md"><mark style="color:blue;"><strong>setScale</strong></mark></a></td><td>Set object scale</td><td><a href="https://codesandbox.io/p/sandbox/transformations-frrd3q">Transformations</a></td></tr></tbody></table>

***



### Materials

<table><thead><tr><th width="50.265625">#</th><th width="186.34375">Method</th><th width="285.59375">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>21</td><td><a href="getallmaterials-new.md"><mark style="color:blue;"><strong>getAllMaterials</strong></mark></a></td><td>Get all materials in the scene</td><td><a href="https://codesandbox.io/p/sandbox/getallmaterials-6vd7vc">getAllMaterials</a></td></tr><tr><td>22</td><td><a href="getmaterials-new.md"><mark style="color:blue;"><strong>getMaterials</strong></mark></a></td><td>Get materials assigned to an object</td><td><a href="https://codesandbox.io/p/sandbox/getmaterials-dfcp8h">getMaterials</a></td></tr><tr><td>23</td><td><a href="getactivematerial-new.md"><mark style="color:blue;"><strong>getActiveMaterial</strong></mark></a></td><td>Get active material of an object</td><td><a href="https://codesandbox.io/p/sandbox/get-setactivematerial-49cxf4">get-setActiveMaterial</a></td></tr><tr><td>24</td><td><a href="setactivematerial-new.md"><mark style="color:blue;"><strong>setActiveMaterial</strong></mark></a></td><td>Set active material of an object</td><td><a href="https://codesandbox.io/p/sandbox/get-setactivematerial-49cxf4">get-setActiveMaterial</a></td></tr><tr><td>25</td><td><a href="addoreditmaterial-new.md"><mark style="color:blue;"><strong>addOrEditMaterial</strong></mark></a></td><td>Add new or edit existing material</td><td><a href="https://codesandbox.io/p/sandbox/addoreditmaterial-49cxf4">addOrEditMaterial</a></td></tr><tr><td>26</td><td><a href="removematerial-new.md"><mark style="color:blue;"><strong>removeMaterial</strong></mark></a></td><td>Remove material from an object</td><td><a href="https://codesandbox.io/p/sandbox/removematerial-7w66wz">removeMaterial</a></td></tr></tbody></table>

***



### Textures

<table><thead><tr><th width="51.5078125">#</th><th width="170.58203125">Method</th><th width="290.41796875">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>27</td><td><a href="gettexturedata-new.md"><mark style="color:blue;"><strong>getTextureData</strong></mark></a></td><td>Get texture raw data</td><td><a href="https://codesandbox.io/p/sandbox/get-settexturedata-s25wct">get-setTextureData</a></td></tr><tr><td>28</td><td><a href="settexturedata-new.md"><mark style="color:blue;"><strong>setTextureData</strong></mark></a></td><td>Set texture raw data</td><td><a href="https://codesandbox.io/p/sandbox/get-settexturedata-s25wct">get-setTextureData</a></td></tr><tr><td>29</td><td><a href="addtexture-new.md"><mark style="color:blue;"><strong>addTexture</strong></mark></a></td><td>Add new texture from file</td><td><a href="https://codesandbox.io/p/sandbox/add-maptextures-8d2mkn">add-mapTextures</a></td></tr><tr><td>30</td><td><a href="maptextures-new.md"><mark style="color:blue;"><strong>mapTextures</strong></mark></a></td><td>Overlay texture with positioning</td><td><a href="https://codesandbox.io/p/sandbox/add-maptextures-8d2mkn">add-mapTextures</a></td></tr></tbody></table>

***



### Primitives

<table><thead><tr><th width="47.39453125">#</th><th width="193.953125">Method</th><th>Description</th><th>Snippet</th></tr></thead><tbody><tr><td>31</td><td><a href="getprimitives-new.md"><mark style="color:blue;"><strong>getPrimitives</strong></mark></a></td><td>Get primitive settings</td><td><a href="https://codesandbox.io/p/sandbox/get-setprimitives-g9smpy">get-setPrimitives</a></td></tr><tr><td>32</td><td><a href="setprimitives-new.md"><mark style="color:blue;"><strong>setPrimitives</strong></mark></a></td><td>Set primitive settings</td><td><a href="https://codesandbox.io/p/sandbox/get-setprimitives-g9smpy">get-setPrimitives</a></td></tr></tbody></table>

***



### 3D Text

<table><thead><tr><th width="47.27734375">#</th><th>Method</th><th width="281.33203125">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>33</td><td><a href="gettext3d-new.md"><mark style="color:blue;"><strong>getText3d</strong></mark></a></td><td>Get 3D text settings</td><td><a href="https://codesandbox.io/p/sandbox/get-settext3d-yhvdmr">get-setText3d</a></td></tr><tr><td>34</td><td><a href="settext3d-new.md"><mark style="color:blue;"><strong>setText3d</strong></mark></a></td><td>Set 3D text settings</td><td><a href="https://codesandbox.io/p/sandbox/get-settext3d-yhvdmr">get-setText3d</a></td></tr></tbody></table>

***



### Camera

<table><thead><tr><th width="48.46875">#</th><th>Method</th><th width="300.109375">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>35</td><td><a href="getviewstate-new.md"><mark style="color:blue;"><strong>getViewState</strong></mark></a></td><td>Get camera position and target</td><td><a href="https://codesandbox.io/p/sandbox/get-setviewstate-tkxns3">get-setViewState</a></td></tr><tr><td>36</td><td><a href="setviewstate-new.md"><mark style="color:blue;"><strong>setViewState</strong></mark></a></td><td>Set camera position and target</td><td><a href="https://codesandbox.io/p/sandbox/get-setviewstate-tkxns3">get-setViewState</a></td></tr><tr><td>37</td><td><a href="fittoview-new.md"><mark style="color:blue;"><strong>fitToView</strong></mark></a></td><td>Fit object in camera view</td><td><a href="https://codesandbox.io/p/sandbox/fittoview-yzjv4f">fitToView</a></td></tr></tbody></table>

***



### Animations

<table><thead><tr><th width="51.19921875">#</th><th>Method</th><th width="284.296875">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>38</td><td><a href="getanimations-new.md"><mark style="color:blue;"><strong>getAnimations</strong></mark></a></td><td>Get list of animations</td><td><a href="https://codesandbox.io/p/sandbox/animations-player-qx28q2">Animation Player</a></td></tr><tr><td>39</td><td><a href="playanimation-new.md"><mark style="color:blue;"><strong>playAnimation</strong></mark></a></td><td>Play animation</td><td><a href="https://codesandbox.io/p/sandbox/animations-player-qx28q2">Animation Player</a></td></tr><tr><td>40</td><td><a href="stopanimation-new.md"><mark style="color:blue;"><strong>stopAnimation</strong></mark></a></td><td>Stop animation</td><td><a href="https://codesandbox.io/p/sandbox/animations-player-qx28q2">Animation Player</a></td></tr><tr><td>41</td><td><a href="setanimationplayhead-new.md"><mark style="color:blue;"><strong>setAnimationPlayhead</strong></mark></a></td><td>Set animation progress (0-100)</td><td><a href="https://codesandbox.io/p/sandbox/animations-player-qx28q2">Animation Player</a></td></tr></tbody></table>

***



### Raycast

<table><thead><tr><th width="49.93359375">#</th><th width="204.9765625">Method</th><th width="278.5078125">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>42</td><td><a href="raycastall-new.md"><mark style="color:blue;"><strong>raycastAll</strong></mark></a></td><td>Raycast from current mouse position</td><td><a href="https://codesandbox.io/p/sandbox/get-settexturedata-s25wct">get-setTextureData</a></td></tr><tr><td>43</td><td><a href="raycastobject-new.md"><mark style="color:blue;"><strong>raycastObject</strong></mark></a></td><td>Raycast specific object</td><td><a href="https://codesandbox.io/p/sandbox/getrayfromcoordinate-j85dp8">getRayFromCoordinate</a></td></tr><tr><td>44</td><td><a href="getrayfromcoordinate-new.md"><mark style="color:blue;"><strong>getRayFromCoordinate</strong></mark></a></td><td>Get ray from screen coordinates</td><td><a href="https://codesandbox.io/p/sandbox/getrayfromcoordinate-j85dp8">getRayFromCoordinate</a></td></tr></tbody></table>

***



### Environment

<table><thead><tr><th width="47.91015625">#</th><th width="205.90234375">Method</th><th width="261.875">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>45</td><td><a href="rotateenvironmentmap-new.md"><mark style="color:blue;"><strong>rotateEnvironmentMap</strong></mark></a></td><td>Rotate HDRI environment (degrees)</td><td><a href="https://codesandbox.io/p/sandbox/rotateenvironmentmap-kz3s95">rotateEnvironmentMap</a></td></tr></tbody></table>

***



### Import / Export

<table><thead><tr><th width="55.2265625">#</th><th width="158.5078125">Method</th><th width="329.25">Description</th><th>Snippet</th></tr></thead><tbody><tr><td>46</td><td><a href="importfiles-new.md"><mark style="color:blue;"><strong>importFiles</strong></mark></a></td><td>Import 3D file into scene</td><td><a href="https://codesandbox.io/p/sandbox/importfiles-83tnhj">importFiles</a></td></tr><tr><td>47</td><td><a href="importproject-new.md"><mark style="color:blue;"><strong>importProject</strong></mark></a></td><td>Import another Vectary project</td><td><a href="https://codesandbox.io/p/sandbox/importproject-4nldyf">importProject</a></td></tr><tr><td>48</td><td><a href="exportfile-new.md"><mark style="color:blue;"><strong>exportFile</strong></mark></a></td><td>Export scene to file</td><td><a href="https://codesandbox.io/p/sandbox/exportfile-wdsn8r">exportFile</a></td></tr><tr><td>49</td><td><a href="takescreenshot-new.md"><mark style="color:blue;"><strong>takeScreenshot</strong></mark></a></td><td>Take screenshot of the scene</td><td><a href="https://codesandbox.io/s/takescreenshot-pgy6gf">takeScreenshot</a></td></tr></tbody></table>



***







## Common Types

> Types that appear in multiple methods are documented here. Types specific to a single method are described on that method's page.



### Vector3

3D coordinates or RGB color values.

```typescript
type Vector3 = {
  x: number;
  y: number;
  z: number;
};
```



### Euler

Rotation angles in degrees.

```typescript
type Euler = {
  x: number;
  y: number;
  z: number;
  order?: string; // default: 'XYZ'
};
```



### Object

Scene object returned by `getObjects()` and similar methods.

```typescript
type Object = {
  id: string;
  name: string;
  type: SceneObjects;
  position: Vector3;
  rotation: Euler;
  scale: Vector3;
  materials?: Material[];
  primitive?: PrimitiveNodeSettings;
  text3d?: Text3DNodeSettings;
};
```



### ConfigurationState

State of variants and materials, returned by `getConfigurationState()`.

```typescript
type ConfigurationState = VariantSwitcherData | MaterialSwitcherData;

type VariantSwitcherData = {
  variant: string;
  variant_instanceId: string;
  active_object: string;
  active_object_instanceId: string;
};

type MaterialSwitcherData = {
  object: string;
  object_instanceId: string;
  active_material: string;
  active_material_instanceId: string;
};
```



### CameraViewState

Camera position and orientation, used by `getViewState()` and `setViewState()`.

```typescript
type CameraViewState = {
  target: Vector3;
  position: Vector3;
  upVector: Vector3;
};
```



### Material

Material properties for PBR rendering.

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
	refraction?: {
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

