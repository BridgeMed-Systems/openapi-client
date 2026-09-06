
# UpdateProductMetadataRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`description` | string
`metadata_revision` | number
`device_identifier` | string
`model_number` | string
`specialties` | Array&lt;string&gt;
`procedure_types` | Array&lt;string&gt;

## Example

```typescript
import type { UpdateProductMetadataRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "name": null,
  "description": null,
  "metadata_revision": null,
  "device_identifier": null,
  "model_number": null,
  "specialties": null,
  "procedure_types": null,
} satisfies UpdateProductMetadataRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateProductMetadataRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


