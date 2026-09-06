
# DocumentRevisionInput


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

## Example

```typescript
import type { DocumentRevisionInput } from ''

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
} satisfies DocumentRevisionInput

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DocumentRevisionInput
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


