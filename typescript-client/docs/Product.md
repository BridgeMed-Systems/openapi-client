
# Product


## Properties

Name | Type
------------ | -------------
`device_identifier` | string
`model_number` | string
`specialties` | Array&lt;string&gt;
`procedure_types` | Array&lt;string&gt;
`metadata_revision` | number
`id` | string
`name` | string
`description` | string
`date_added` | Date
`date_updated` | Date
`vendor_org_id` | string

## Example

```typescript
import type { Product } from ''

// TODO: Update the object below with actual values
const example = {
  "device_identifier": null,
  "model_number": null,
  "specialties": null,
  "procedure_types": null,
  "metadata_revision": null,
  "id": null,
  "name": null,
  "description": null,
  "date_added": null,
  "date_updated": null,
  "vendor_org_id": null,
} satisfies Product

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Product
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


