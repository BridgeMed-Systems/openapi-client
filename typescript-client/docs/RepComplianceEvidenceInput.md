
# RepComplianceEvidenceInput


## Properties

Name | Type
------------ | -------------
`provider_name` | string
`evidence_reference` | string
`evidence_url` | string
`notes` | string
`completed_on` | string
`expires_on` | string
`verified` | boolean

## Example

```typescript
import type { RepComplianceEvidenceInput } from ''

// TODO: Update the object below with actual values
const example = {
  "provider_name": null,
  "evidence_reference": null,
  "evidence_url": null,
  "notes": null,
  "completed_on": null,
  "expires_on": null,
  "verified": null,
} satisfies RepComplianceEvidenceInput

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepComplianceEvidenceInput
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


