
# CreateManagedDocumentRequest


## Properties

Name | Type
------------ | -------------
`product_id` | string
`category` | string
`revision` | [DocumentRevisionInput](DocumentRevisionInput.md)

## Example

```typescript
import type { CreateManagedDocumentRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "product_id": null,
  "category": null,
  "revision": null,
} satisfies CreateManagedDocumentRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateManagedDocumentRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


