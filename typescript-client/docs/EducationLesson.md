
# EducationLesson


## Properties

Name | Type
------------ | -------------
`id` | string
`position` | number
`title` | string
`body` | string
`document_id` | string
`acknowledgement_required` | boolean

## Example

```typescript
import type { EducationLesson } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "position": null,
  "title": null,
  "body": null,
  "document_id": null,
  "acknowledgement_required": null,
} satisfies EducationLesson

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EducationLesson
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


