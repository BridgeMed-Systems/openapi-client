
# ManagedDocument


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`product_id` | string
`category` | string
`title` | string
`description` | string
`hidden` | boolean
`current` | [DocumentRevision](DocumentRevision.md)
`revisions` | [Array&lt;DocumentRevision&gt;](DocumentRevision.md)

## Example

```typescript
import type { ManagedDocument } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "product_id": null,
  "category": null,
  "title": null,
  "description": null,
  "hidden": null,
  "current": null,
  "revisions": null,
} satisfies ManagedDocument

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ManagedDocument
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


