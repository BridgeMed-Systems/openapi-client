
# NativeParticipant


## Properties

Name | Type
------------ | -------------
`id` | string
`name` | string
`seat_kind` | string
`tracks` | [Array&lt;NativeTrack&gt;](NativeTrack.md)

## Example

```typescript
import type { NativeParticipant } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "name": null,
  "seat_kind": null,
  "tracks": null,
} satisfies NativeParticipant

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as NativeParticipant
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


