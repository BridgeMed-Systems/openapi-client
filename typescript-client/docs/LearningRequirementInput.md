
# LearningRequirementInput


## Properties

Name | Type
------------ | -------------
`version_id` | string
`title` | string
`scope` | string
`member_user_id` | string
`department_id` | string
`due_days` | number
`valid_days` | number

## Example

```typescript
import type { LearningRequirementInput } from ''

// TODO: Update the object below with actual values
const example = {
  "version_id": null,
  "title": null,
  "scope": null,
  "member_user_id": null,
  "department_id": null,
  "due_days": null,
  "valid_days": null,
} satisfies LearningRequirementInput

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LearningRequirementInput
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


