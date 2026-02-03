# projectInfo \[new]



#### projectInfo



Returns information about the current project.



#### Signature

```typescript
projectInfo(): Promise<ProjectInfo>
```

#### Parameters



None.



#### Returns

`Promise<ProjectInfo>` — Object containing project details:

```typescript
type ProjectInfo = {
  projectName: string;
  modelId: string;
  modelIdBase62: string;
  publishedId: string;
  workspaceId: string;
}
```

| Property      | Type   | Description                    |
| ------------- | ------ | ------------------------------ |
| projectName   | string | Name of the project            |
| modelId       | string | Unique model identifier (UUID) |
| modelIdBase62 | string | Model ID in Base62 format      |
| publishedId   | string | Published version identifier   |
| workspaceId   | string | Workspace identifier           |

#### Usage

```javascript
const info = await api.projectInfo();
console.log(info.projectName);
console.log(info.modelId);
```
