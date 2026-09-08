
# FeatureSettings


## Properties

Name | Type
------------ | -------------
`billing_enabled` | boolean
`native_rooms_enabled` | boolean
`documents_enabled` | boolean
`email_enabled` | boolean

## Example

```typescript
import type { FeatureSettings } from ''

// TODO: Update the object below with actual values
const example = {
  "billing_enabled": null,
  "native_rooms_enabled": null,
  "documents_enabled": null,
  "email_enabled": null,
} satisfies FeatureSettings

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as FeatureSettings
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


