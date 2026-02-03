---
hidden: true
---

# projectInfo

Returns some basic information about the model: `ProjectInfo`

```typescript
projectInfo(): Promise<ProjectInfo>
```

Usage:

```javascript
await modelApi.projectInfo();
```

Return value example:

```javascript
{
    "projectName": "Goggles AR",
    "modelId": "7bcf5c5e-8b16-4dc8-897f-a7965bae9aaa",
    "modelIdBase62": "3lcorX14cyHmKcW3LNr66s",
    "publishedId": "e63ae0af-53a5-4087-af83-d4ed36c8a46e",
    "workspaceId": "d8909d2c-feec-443d-891f-f42fce66bca4"
}
```







