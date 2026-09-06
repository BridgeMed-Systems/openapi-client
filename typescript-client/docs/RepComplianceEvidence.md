
# RepComplianceEvidence


## Properties

Name | Type
------------ | -------------
`id` | string
`requirement_id` | string
`organization_id` | string
`rep_user_id` | string
`vendor_org_id` | string
`provider_name` | string
`evidence_reference` | string
`evidence_url` | string
`notes` | string
`completed_on` | string
`expires_on` | string
`recorded_by_user_id` | string
`recorded_at` | Date
`voided_at` | Date
`voided_by_user_id` | string
`void_reason` | string

## Example

```typescript
import type { RepComplianceEvidence } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "requirement_id": null,
  "organization_id": null,
  "rep_user_id": null,
  "vendor_org_id": null,
  "provider_name": null,
  "evidence_reference": null,
  "evidence_url": null,
  "notes": null,
  "completed_on": null,
  "expires_on": null,
  "recorded_by_user_id": null,
  "recorded_at": null,
  "voided_at": null,
  "voided_by_user_id": null,
  "void_reason": null,
} satisfies RepComplianceEvidence

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepComplianceEvidence
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


