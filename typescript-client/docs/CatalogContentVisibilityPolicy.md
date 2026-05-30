
# CatalogContentVisibilityPolicy


## Properties

Name | Type
------------ | -------------
`id` | string
`hospital_organization_id` | string
`vendor_organization_id` | string
`product_id` | string
`content_type` | [CatalogContentType](CatalogContentType.md)
`content_item_id` | string
`effect` | [CatalogContentVisibilityPolicyEffect](CatalogContentVisibilityPolicyEffect.md)
`reason` | string
`created_by_user_id` | string
`updated_by_user_id` | string
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { CatalogContentVisibilityPolicy } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "hospital_organization_id": null,
  "vendor_organization_id": null,
  "product_id": null,
  "content_type": null,
  "content_item_id": null,
  "effect": null,
  "reason": null,
  "created_by_user_id": null,
  "updated_by_user_id": null,
  "date_added": null,
  "date_updated": null,
} satisfies CatalogContentVisibilityPolicy

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CatalogContentVisibilityPolicy
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


