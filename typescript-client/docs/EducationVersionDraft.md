
# EducationVersionDraft


## Properties

Name | Type
------------ | -------------
`title` | string
`summary` | string
`pass_percent` | number
`credit_type` | string
`credit_amount` | string
`provider_name` | string
`provider_reference` | string
`certificate_label` | string
`valid_days` | number
`lessons` | [Array&lt;EducationLessonDraft&gt;](EducationLessonDraft.md)
`questions` | [Array&lt;EducationQuestionDraft&gt;](EducationQuestionDraft.md)

## Example

```typescript
import type { EducationVersionDraft } from ''

// TODO: Update the object below with actual values
const example = {
  "title": null,
  "summary": null,
  "pass_percent": null,
  "credit_type": null,
  "credit_amount": null,
  "provider_name": null,
  "provider_reference": null,
  "certificate_label": null,
  "valid_days": null,
  "lessons": null,
  "questions": null,
} satisfies EducationVersionDraft

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EducationVersionDraft
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


