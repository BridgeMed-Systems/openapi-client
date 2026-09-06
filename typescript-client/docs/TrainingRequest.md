
# TrainingRequest


## Properties

Name | Type
------------ | -------------
`request_type` | string
`product_name` | string
`organization_name` | string
`requester_name` | string
`requester_email` | string
`requester_phone` | string
`id` | string
`organization_id` | string
`submitted_by_user_id` | string
`assigned_user_id` | string
`product_id` | string
`title` | string
`message` | string
`status` | [TrainingRequestStatus](TrainingRequestStatus.md)
`session_id` | string
`scheduled_start_at` | Date
`scheduled_end_at` | Date
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { TrainingRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "request_type": null,
  "product_name": null,
  "organization_name": null,
  "requester_name": null,
  "requester_email": null,
  "requester_phone": null,
  "id": null,
  "organization_id": null,
  "submitted_by_user_id": null,
  "assigned_user_id": null,
  "product_id": null,
  "title": null,
  "message": null,
  "status": null,
  "session_id": null,
  "scheduled_start_at": null,
  "scheduled_end_at": null,
  "date_added": null,
  "date_updated": null,
} satisfies TrainingRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TrainingRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


