
# LearningCompletion


## Properties

Name | Type
------------ | -------------
`id` | string
`attempt_id` | string
`enrollment_id` | string
`organization_id` | string
`user_id` | string
`version_id` | string
`course_title` | string
`course_version_number` | number
`learner_name` | string
`hospital_name` | string
`vendor_name` | string
`credit_type` | string
`credit_amount` | string
`provider_name` | string
`provider_reference` | string
`certificate_label` | string
`score_percent` | number
`completed_at` | Date
`expires_at` | Date

## Example

```typescript
import type { LearningCompletion } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "attempt_id": null,
  "enrollment_id": null,
  "organization_id": null,
  "user_id": null,
  "version_id": null,
  "course_title": null,
  "course_version_number": null,
  "learner_name": null,
  "hospital_name": null,
  "vendor_name": null,
  "credit_type": null,
  "credit_amount": null,
  "provider_name": null,
  "provider_reference": null,
  "certificate_label": null,
  "score_percent": null,
  "completed_at": null,
  "expires_at": null,
} satisfies LearningCompletion

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LearningCompletion
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


