
# LearningRequirement


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`version_id` | string
`title` | string
`scope` | string
`member_user_id` | string
`department_id` | string
`due_days` | number
`valid_days` | number
`course_title` | string
`course_version_number` | number
`enabled` | boolean
`available` | boolean
`scope_name` | string
`created_at` | Date
`disabled_at` | Date
`assigned_count` | number
`completed_count` | number

## Example

```typescript
import type { LearningRequirement } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "version_id": null,
  "title": null,
  "scope": null,
  "member_user_id": null,
  "department_id": null,
  "due_days": null,
  "valid_days": null,
  "course_title": null,
  "course_version_number": null,
  "enabled": null,
  "available": null,
  "scope_name": null,
  "created_at": null,
  "disabled_at": null,
  "assigned_count": null,
  "completed_count": null,
} satisfies LearningRequirement

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LearningRequirement
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


