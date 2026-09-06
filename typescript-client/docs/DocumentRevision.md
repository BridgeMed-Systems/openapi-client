
# DocumentRevision


## Properties

Name | Type
------------ | -------------
`caption_language` | string
`caption_label` | string
`captions_vtt` | string
`revision_label` | string
`publication_date` | Date
`title` | string
`description` | string
`file_name` | string
`media_type` | string
`byte_size` | number
`sha256` | string
`id` | string
`content_id` | string
`organization_id` | string
`processing_state` | string
`publication_state` | string
`created_at` | Date
`published_at` | Date
`withdrawn_at` | Date
`withdrawal_reason` | string
`failure_reason` | string
`main_asset_name` | string
`duration_seconds` | number

## Example

```typescript
import type { DocumentRevision } from ''

// TODO: Update the object below with actual values
const example = {
  "caption_language": null,
  "caption_label": null,
  "captions_vtt": null,
  "revision_label": null,
  "publication_date": null,
  "title": null,
  "description": null,
  "file_name": null,
  "media_type": null,
  "byte_size": null,
  "sha256": null,
  "id": null,
  "content_id": null,
  "organization_id": null,
  "processing_state": null,
  "publication_state": null,
  "created_at": null,
  "published_at": null,
  "withdrawn_at": null,
  "withdrawal_reason": null,
  "failure_reason": null,
  "main_asset_name": null,
  "duration_seconds": null,
} satisfies DocumentRevision

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DocumentRevision
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


