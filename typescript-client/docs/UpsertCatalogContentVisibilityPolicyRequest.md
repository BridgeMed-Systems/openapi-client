
# UpsertCatalogContentVisibilityPolicyRequest


## Properties

Name | Type
------------ | -------------
`vendor_organization_id` | string
`product_id` | string
`content_type` | [CatalogContentType](CatalogContentType.md)
`content_item_id` | string
`effect` | [CatalogContentVisibilityPolicyEffect](CatalogContentVisibilityPolicyEffect.md)
`reason` | string

## Example

```typescript
import type { UpsertCatalogContentVisibilityPolicyRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "vendor_organization_id": null,
  "product_id": null,
  "content_type": null,
  "content_item_id": null,
  "effect": null,
  "reason": null,
} satisfies UpsertCatalogContentVisibilityPolicyRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpsertCatalogContentVisibilityPolicyRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


