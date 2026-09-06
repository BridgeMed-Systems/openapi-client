
# EducationCourse


## Properties

Name | Type
------------ | -------------
`id` | string
`organization_id` | string
`organization_name` | string
`product_id` | string
`product_name` | string
`current_version_id` | string
`title` | string
`created_at` | Date
`versions` | [Array&lt;EducationVersion&gt;](EducationVersion.md)

## Example

```typescript
import type { EducationCourse } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "organization_id": null,
  "organization_name": null,
  "product_id": null,
  "product_name": null,
  "current_version_id": null,
  "title": null,
  "created_at": null,
  "versions": null,
} satisfies EducationCourse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EducationCourse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


