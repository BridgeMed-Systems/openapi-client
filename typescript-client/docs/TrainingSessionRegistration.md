
# TrainingSessionRegistration


## Properties

Name | Type
------------ | -------------
`id` | string
`session_id` | string
`user_id` | string
`attendance_status` | [TrainingSessionAttendanceStatus](TrainingSessionAttendanceStatus.md)
`checked_in_at` | Date
`registered_by_user_id` | string
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { TrainingSessionRegistration } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "session_id": null,
  "user_id": null,
  "attendance_status": null,
  "checked_in_at": null,
  "registered_by_user_id": null,
  "date_added": null,
  "date_updated": null,
} satisfies TrainingSessionRegistration

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrainingSessionRegistration
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


