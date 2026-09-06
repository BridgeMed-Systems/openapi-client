
# LearningEnrollment


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`user_id` | string
`version_id` | string
`course_title` | string
`course_version_number` | number
`learner_name` | string
`department_id` | string
`department_name` | string
`created_at` | Date
`self_enrolled_at` | Date
`state` | string
`available` | boolean
`required_count` | number
`due_at` | Date
`compliance_expires_at` | Date
`current_attempt_id` | string
`completion` | [LearningCompletion](LearningCompletion.md)

## Example

```typescript
import type { LearningEnrollment } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "user_id": null,
  "version_id": null,
  "course_title": null,
  "course_version_number": null,
  "learner_name": null,
  "department_id": null,
  "department_name": null,
  "created_at": null,
  "self_enrolled_at": null,
  "state": null,
  "available": null,
  "required_count": null,
  "due_at": null,
  "compliance_expires_at": null,
  "current_attempt_id": null,
  "completion": null,
} satisfies LearningEnrollment

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LearningEnrollment
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


