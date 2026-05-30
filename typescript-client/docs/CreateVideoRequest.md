
# CreateVideoRequest


## Properties

Name | Type
------------ | -------------
`organization_id` | string
`product_id` | string
`title` | string
`description` | string
`upload_content_type` | string
`upload_size_bytes` | number

## Example

```typescript
import type { CreateVideoRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "organization_id": null,
  "product_id": null,
  "title": null,
  "description": null,
  "upload_content_type": null,
  "upload_size_bytes": null,
} satisfies CreateVideoRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateVideoRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


