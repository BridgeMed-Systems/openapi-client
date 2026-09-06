
# EducationVersion


## Properties

Name | Type
------------ | -------------
`id` | string
`course_id` | string
`organization_id` | string
`number` | number
`title` | string
`summary` | string
`pass_percent` | number
`credit_type` | string
`credit_amount` | string
`provider_name` | string
`provider_reference` | string
`certificate_label` | string
`valid_days` | number
`state` | string
`published_at` | Date
`withdrawn_at` | Date
`withdrawal_reason` | string
`created_at` | Date
`lessons` | [Array&lt;EducationLesson&gt;](EducationLesson.md)
`questions` | [Array&lt;EducationQuestion&gt;](EducationQuestion.md)

## Example

```typescript
import type { EducationVersion } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "course_id": null,
  "organization_id": null,
  "number": null,
  "title": null,
  "summary": null,
  "pass_percent": null,
  "credit_type": null,
  "credit_amount": null,
  "provider_name": null,
  "provider_reference": null,
  "certificate_label": null,
  "valid_days": null,
  "state": null,
  "published_at": null,
  "withdrawn_at": null,
  "withdrawal_reason": null,
  "created_at": null,
  "lessons": null,
  "questions": null,
} satisfies EducationVersion

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EducationVersion
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


