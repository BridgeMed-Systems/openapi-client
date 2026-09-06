
# DocumentAction


## Properties

Name | Type
------------ | -------------
`id` | string
`title` | string
`category` | string
`available` | boolean
`managed` | boolean
`revision_label` | string
`publication_date` | Date

## Example

```typescript
import type { DocumentAction } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "title": null,
  "category": null,
  "available": null,
  "managed": null,
  "revision_label": null,
  "publication_date": null,
} satisfies DocumentAction

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DocumentAction
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


