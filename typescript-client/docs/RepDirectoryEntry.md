
# RepDirectoryEntry


## Properties

Name | Type
------------ | -------------
`title` | string
`user_id` | string
`first_name` | string
`last_name` | string
`email` | string
`phone_number` | string
`vendor_organization_id` | string
`vendor_organization_name` | string
`product_ids` | Array&lt;string&gt;
`product_names` | Array&lt;string&gt;
`account_organization_ids` | Array&lt;string&gt;
`account_organization_names` | Array&lt;string&gt;

## Example

```typescript
import type { RepDirectoryEntry } from ''

// TODO: Update the object below with actual values
const example = {
  "title": null,
  "user_id": null,
  "first_name": null,
  "last_name": null,
  "email": null,
  "phone_number": null,
  "vendor_organization_id": null,
  "vendor_organization_name": null,
  "product_ids": null,
  "product_names": null,
  "account_organization_ids": null,
  "account_organization_names": null,
} satisfies RepDirectoryEntry

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepDirectoryEntry
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


