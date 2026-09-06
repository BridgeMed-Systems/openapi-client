
# EventHistoryItem


## Properties

Name | Type
------------ | -------------
`id` | string
`source_type` | string
`source_id` | string
`title` | string
`starts_at` | Date
`ends_at` | Date
`attendance_status` | string
`attendance_source` | string
`attendance_evidence` | string
`verified_seconds` | number
`checked_in_at` | Date
`registered_at` | Date
`event_available` | boolean
`event_status` | string

## Example

```typescript
import type { EventHistoryItem } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "source_type": null,
  "source_id": null,
  "title": null,
  "starts_at": null,
  "ends_at": null,
  "attendance_status": null,
  "attendance_source": null,
  "attendance_evidence": null,
  "verified_seconds": null,
  "checked_in_at": null,
  "registered_at": null,
  "event_available": null,
  "event_status": null,
} satisfies EventHistoryItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EventHistoryItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


