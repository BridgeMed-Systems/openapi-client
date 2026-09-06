
# VendorPrice


## Properties

Name | Type
------------ | -------------
`plan_key` | string
`plan_name` | string
`interval` | string
`amount` | number
`currency` | string
`tax_behavior` | string

## Example

```typescript
import type { VendorPrice } from ''

// TODO: Update the object below with actual values
const example = {
  "plan_key": null,
  "plan_name": null,
  "interval": null,
  "amount": null,
  "currency": null,
  "tax_behavior": null,
} satisfies VendorPrice

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VendorPrice
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


