
# DeviceSearchItem


## Properties

Name | Type
------------ | -------------
`in_library` | boolean
`product` | [Product](Product.md)
`vendor_name` | string
`documents` | [Array&lt;DocumentAction&gt;](DocumentAction.md)

## Example

```typescript
import type { DeviceSearchItem } from ''

// TODO: Update the object below with actual values
const example = {
  "in_library": null,
  "product": null,
  "vendor_name": null,
  "documents": null,
} satisfies DeviceSearchItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DeviceSearchItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


