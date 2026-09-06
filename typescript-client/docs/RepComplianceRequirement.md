
# RepComplianceRequirement


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`rep_user_id` | string
`vendor_org_id` | string
`title` | string
`instructions` | string
`due_on` | string
`rep_name` | string
`vendor_name` | string
`enabled` | boolean
`eligible` | boolean
`state` | string
`created_at` | Date
`current_evidence` | [RepComplianceEvidence](RepComplianceEvidence.md)

## Example

```typescript
import type { RepComplianceRequirement } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "rep_user_id": null,
  "vendor_org_id": null,
  "title": null,
  "instructions": null,
  "due_on": null,
  "rep_name": null,
  "vendor_name": null,
  "enabled": null,
  "eligible": null,
  "state": null,
  "created_at": null,
  "current_evidence": null,
} satisfies RepComplianceRequirement

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepComplianceRequirement
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


