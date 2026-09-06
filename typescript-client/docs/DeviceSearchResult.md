
# DeviceSearchResult


## Properties

Name | Type
------------ | -------------
`items` | [Array&lt;DeviceSearchItem&gt;](DeviceSearchItem.md)
`total` | number
`limit` | number
`offset` | number
`vendors` | [Array&lt;CatalogVendor&gt;](CatalogVendor.md)
`specialties` | Array&lt;string&gt;
`procedure_types` | Array&lt;string&gt;

## Example

```typescript
import type { DeviceSearchResult } from ''

// TODO: Update the object below with actual values
const example = {
  "items": null,
  "total": null,
  "limit": null,
  "offset": null,
  "vendors": null,
  "specialties": null,
  "procedure_types": null,
} satisfies DeviceSearchResult

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DeviceSearchResult
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


