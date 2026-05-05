
# UpdateTrainingRequestStatusRequest


## Properties

Name | Type
------------ | -------------
`status` | [TrainingRequestStatus](TrainingRequestStatus.md)
`assigned_user_id` | string
`scheduled_start_at` | Date
`scheduled_end_at` | Date
`delivery_mode` | [TrainingSessionDeliveryMode](TrainingSessionDeliveryMode.md)
`location_text` | string
`external_join_url` | string
`capacity` | number

## Example

```typescript
import type { UpdateTrainingRequestStatusRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "status": null,
  "assigned_user_id": null,
  "scheduled_start_at": null,
  "scheduled_end_at": null,
  "delivery_mode": null,
  "location_text": null,
  "external_join_url": null,
  "capacity": null,
} satisfies UpdateTrainingRequestStatusRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateTrainingRequestStatusRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


