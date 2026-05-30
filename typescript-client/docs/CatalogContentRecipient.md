
# CatalogContentRecipient


## Properties

Name | Type
------------ | -------------
`organization` | [CatalogContentRecipientOrganization](CatalogContentRecipientOrganization.md)
`eligible` | boolean
`visible` | boolean
`policy_effect` | [CatalogContentVisibilityPolicyEffect](CatalogContentVisibilityPolicyEffect.md)
`reasons` | Array&lt;string&gt;

## Example

```typescript
import type { CatalogContentRecipient } from ''

// TODO: Update the object below with actual values
const example = {
  "organization": null,
  "eligible": null,
  "visible": null,
  "policy_effect": null,
  "reasons": null,
} satisfies CatalogContentRecipient

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CatalogContentRecipient
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


