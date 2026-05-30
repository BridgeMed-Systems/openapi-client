
# VideoAsset


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`product_id` | string
`created_by_user_id` | string
`title` | string
`description` | string
`status` | [VideoAssetStatus](VideoAssetStatus.md)
`upload_status` | [VideoUploadStatus](VideoUploadStatus.md)
`playback_status` | [VideoPlaybackStatus](VideoPlaybackStatus.md)
`upload_content_type` | string
`upload_size_bytes` | number
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { VideoAsset } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "product_id": null,
  "created_by_user_id": null,
  "title": null,
  "description": null,
  "status": null,
  "upload_status": null,
  "playback_status": null,
  "upload_content_type": null,
  "upload_size_bytes": null,
  "date_added": null,
  "date_updated": null,
} satisfies VideoAsset

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoAsset
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


