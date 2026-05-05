
# UpdateTrainingSessionMaterialRequest


## Properties

Name | Type
------------ | -------------
`material_kind` | [TrainingSessionMaterialKind](TrainingSessionMaterialKind.md)
`catalog_content_id` | string
`title` | string
`description` | string
`external_url` | string
`upload_filename` | string
`upload_content_type` | string
`upload_size_bytes` | number
`sort_order` | number

## Example

```typescript
import type { UpdateTrainingSessionMaterialRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "material_kind": null,
  "catalog_content_id": null,
  "title": null,
  "description": null,
  "external_url": null,
  "upload_filename": null,
  "upload_content_type": null,
  "upload_size_bytes": null,
  "sort_order": null,
} satisfies UpdateTrainingSessionMaterialRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateTrainingSessionMaterialRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


