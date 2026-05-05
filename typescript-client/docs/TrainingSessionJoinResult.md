
# TrainingSessionJoinResult


## Properties

Name | Type
------------ | -------------
`session_id` | string
`delivery_mode` | [TrainingSessionDeliveryMode](TrainingSessionDeliveryMode.md)
`location_text` | string
`external_join_url` | string
`native_join_result` | [WebinarJoinResult](WebinarJoinResult.md)

## Example

```typescript
import type { TrainingSessionJoinResult } from ''

// TODO: Update the object below with actual values
const example = {
  "session_id": null,
  "delivery_mode": null,
  "location_text": null,
  "external_join_url": null,
  "native_join_result": null,
} satisfies TrainingSessionJoinResult

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrainingSessionJoinResult
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


