
# TrainingSession


## Properties

Name | Type
------------ | -------------
`id` | string
`source_request_id` | string
`organization_id` | string
`product_id` | string
`host_user_id` | string
`title` | string
`description` | string
`delivery_mode` | [TrainingSessionDeliveryMode](TrainingSessionDeliveryMode.md)
`status` | [TrainingSessionStatus](TrainingSessionStatus.md)
`starts_at` | Date
`ends_at` | Date
`location_text` | string
`external_join_url` | string
`capacity` | number
`native_webinar_id` | string
`completed_at` | Date
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { TrainingSession } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "source_request_id": null,
  "organization_id": null,
  "product_id": null,
  "host_user_id": null,
  "title": null,
  "description": null,
  "delivery_mode": null,
  "status": null,
  "starts_at": null,
  "ends_at": null,
  "location_text": null,
  "external_join_url": null,
  "capacity": null,
  "native_webinar_id": null,
  "completed_at": null,
  "date_added": null,
  "date_updated": null,
} satisfies TrainingSession

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrainingSession
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


