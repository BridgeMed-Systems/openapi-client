
# WebinarJoinResult


## Properties

Name | Type
------------ | -------------
`participant_token` | string
`expires_at` | Date
`signal_path` | string
`room_owner_node` | string
`participant_role` | [WebinarParticipantRole](WebinarParticipantRole.md)
`ice_servers` | [Array&lt;WebinarIceServer&gt;](WebinarIceServer.md)
`transport` | string
`admission_id` | string

## Example

```typescript
import type { WebinarJoinResult } from ''

// TODO: Update the object below with actual values
const example = {
  "participant_token": null,
  "expires_at": null,
  "signal_path": null,
  "room_owner_node": null,
  "participant_role": null,
  "ice_servers": null,
  "transport": null,
  "admission_id": null,
} satisfies WebinarJoinResult

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WebinarJoinResult
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


