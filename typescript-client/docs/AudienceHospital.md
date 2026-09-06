
# AudienceHospital


## Properties

Name | Type
------------ | -------------
`organization_id` | string
`name` | string
`eligible` | boolean
`published` | boolean
`hospital_available` | boolean

## Example

```typescript
import type { AudienceHospital } from ''

// TODO: Update the object below with actual values
const example = {
  "organization_id": null,
  "name": null,
  "eligible": null,
  "published": null,
  "hospital_available": null,
} satisfies AudienceHospital

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AudienceHospital
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


