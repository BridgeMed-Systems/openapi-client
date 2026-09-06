
# HospitalStaffMember


## Properties

Name | Type
------------ | -------------
`id` | string
`name` | string
`email` | string
`role` | string
`department_id` | string
`joined_at` | Date

## Example

```typescript
import type { HospitalStaffMember } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "name": null,
  "email": null,
  "role": null,
  "department_id": null,
  "joined_at": null,
} satisfies HospitalStaffMember

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HospitalStaffMember
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


