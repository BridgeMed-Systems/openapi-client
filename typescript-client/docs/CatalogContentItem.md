
# CatalogContentItem


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`product_id` | string
`created_by_user_id` | string
`updated_by_user_id` | string
`title` | string
`description` | string
`content_type` | [CatalogContentType](CatalogContentType.md)
`external_url` | string
`tags` | Array&lt;string&gt;
`status` | [CatalogContentStatus](CatalogContentStatus.md)
`publication_status` | [CatalogContentPublicationStatus](CatalogContentPublicationStatus.md)
`publication_version` | number
`date_added` | Date
`date_updated` | Date
`date_archived` | Date
`date_published` | Date
`date_revoked` | Date

## Example

```typescript
import type { CatalogContentItem } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "product_id": null,
  "created_by_user_id": null,
  "updated_by_user_id": null,
  "title": null,
  "description": null,
  "content_type": null,
  "external_url": null,
  "tags": null,
  "status": null,
  "publication_status": null,
  "publication_version": null,
  "date_added": null,
  "date_updated": null,
  "date_archived": null,
  "date_published": null,
  "date_revoked": null,
} satisfies CatalogContentItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CatalogContentItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


