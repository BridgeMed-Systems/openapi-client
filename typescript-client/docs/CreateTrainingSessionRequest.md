
# CreateTrainingSessionRequest


## Properties

Name | Type
------------ | -------------
`source_request_id` | string
`host_user_id` | string
`title` | string
`description` | string
`delivery_mode` | [TrainingSessionDeliveryMode](TrainingSessionDeliveryMode.md)
`starts_at` | Date
`ends_at` | Date
`location_text` | string
`external_join_url` | string
`capacity` | number

## Example

```typescript
import type { CreateTrainingSessionRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "source_request_id": null,
  "host_user_id": null,
  "title": null,
  "description": null,
  "delivery_mode": null,
  "starts_at": null,
  "ends_at": null,
  "location_text": null,
  "external_join_url": null,
  "capacity": null,
} satisfies CreateTrainingSessionRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateTrainingSessionRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


