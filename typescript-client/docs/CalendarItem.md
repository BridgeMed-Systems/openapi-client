
# CalendarItem


## Properties

Name | Type
------------ | -------------
`source_type` | [CalendarSourceType](CalendarSourceType.md)
`source_id` | string
`organization_id` | string
`title` | string
`description` | string
`start_at` | Date
`end_at` | Date
`can_manage` | boolean
`manage_scope` | [CalendarManageScope](CalendarManageScope.md)
`delivery_mode` | [TrainingSessionDeliveryMode](TrainingSessionDeliveryMode.md)
`location_text` | string
`external_join_url` | string
`status` | string
`sequence` | number
`updated_at` | Date

## Example

```typescript
import type { CalendarItem } from ''

// TODO: Update the object below with actual values
const example = {
  "source_type": null,
  "source_id": null,
  "organization_id": null,
  "title": null,
  "description": null,
  "start_at": null,
  "end_at": null,
  "can_manage": null,
  "manage_scope": null,
  "delivery_mode": null,
  "location_text": null,
  "external_join_url": null,
  "status": null,
  "sequence": null,
  "updated_at": null,
} satisfies CalendarItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CalendarItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


