
# UpdateTrainingSessionRequest


## Properties

Name | Type
------------ | -------------
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
import type { UpdateTrainingSessionRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "title": null,
  "description": null,
  "delivery_mode": null,
  "starts_at": null,
  "ends_at": null,
  "location_text": null,
  "external_join_url": null,
  "capacity": null,
} satisfies UpdateTrainingSessionRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateTrainingSessionRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


