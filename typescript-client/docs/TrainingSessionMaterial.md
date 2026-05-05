
# TrainingSessionMaterial


## Properties

Name | Type
------------ | -------------
`id` | string
`session_id` | string
`material_kind` | [TrainingSessionMaterialKind](TrainingSessionMaterialKind.md)
`catalog_content_id` | string
`title` | string
`description` | string
`external_url` | string
`upload_object_key` | string
`upload_filename` | string
`upload_content_type` | string
`upload_size_bytes` | number
`upload_status` | string
`sort_order` | number
`upload_url` | string
`download_url` | string
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { TrainingSessionMaterial } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "session_id": null,
  "material_kind": null,
  "catalog_content_id": null,
  "title": null,
  "description": null,
  "external_url": null,
  "upload_object_key": null,
  "upload_filename": null,
  "upload_content_type": null,
  "upload_size_bytes": null,
  "upload_status": null,
  "sort_order": null,
  "upload_url": null,
  "download_url": null,
  "date_added": null,
  "date_updated": null,
} satisfies TrainingSessionMaterial

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrainingSessionMaterial
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


