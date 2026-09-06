
# LearningDetail


## Properties

Name | Type
------------ | -------------
`enrollment` | [LearningEnrollment](LearningEnrollment.md)
`version` | [EducationVersion](EducationVersion.md)
`acknowledged_lesson_ids` | Array&lt;string&gt;
`document_revisions` | { [key: string]: string; }

## Example

```typescript
import type { LearningDetail } from ''

// TODO: Update the object below with actual values
const example = {
  "enrollment": null,
  "version": null,
  "acknowledged_lesson_ids": null,
  "document_revisions": null,
} satisfies LearningDetail

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LearningDetail
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


