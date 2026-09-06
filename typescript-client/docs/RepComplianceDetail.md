
# RepComplianceDetail


## Properties

Name | Type
------------ | -------------
`requirement` | [RepComplianceRequirement](RepComplianceRequirement.md)
`history` | [Array&lt;RepComplianceEvidence&gt;](RepComplianceEvidence.md)

## Example

```typescript
import type { RepComplianceDetail } from ''

// TODO: Update the object below with actual values
const example = {
  "requirement": null,
  "history": null,
} satisfies RepComplianceDetail

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepComplianceDetail
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


