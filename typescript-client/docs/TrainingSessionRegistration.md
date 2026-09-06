
# TrainingSessionRegistration

Exactly one of session_id or webinar_id identifies the source event.

## Properties

Name | Type
------------ | -------------
`organization_id` | string
`attendance_source` | string
`attendance_evidence` | string
`recorded_by_user_id` | string
`verified_attendance_seconds` | number
`id` | string
`webinar_id` | string
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
  "organization_id": null,
  "attendance_source": null,
  "attendance_evidence": null,
  "recorded_by_user_id": null,
  "verified_attendance_seconds": null,
  "id": null,
  "webinar_id": null,
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


