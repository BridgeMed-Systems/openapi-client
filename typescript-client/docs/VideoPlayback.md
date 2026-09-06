
# VideoPlayback


## Properties

Name | Type
------------ | -------------
`document_id` | string
`revision_id` | string
`manifest_url` | string
`captions_url` | string
`caption_language` | string
`caption_label` | string

## Example

```typescript
import type { VideoPlayback } from ''

// TODO: Update the object below with actual values
const example = {
  "document_id": null,
  "revision_id": null,
  "manifest_url": null,
  "captions_url": null,
  "caption_language": null,
  "caption_label": null,
} satisfies VideoPlayback

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoPlayback
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


