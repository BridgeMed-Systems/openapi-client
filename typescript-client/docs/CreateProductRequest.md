
# CreateProductRequest


## Properties

Name | Type
------------ | -------------
`device_identifier` | string
`model_number` | string
`specialties` | Array&lt;string&gt;
`procedure_types` | Array&lt;string&gt;
`name` | string
`description` | string
`vendor_org_id` | string

## Example

```typescript
import type { CreateProductRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "device_identifier": null,
  "model_number": null,
  "specialties": null,
  "procedure_types": null,
  "name": null,
  "description": null,
  "vendor_org_id": null,
} satisfies CreateProductRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateProductRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


