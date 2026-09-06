
# EventParticipationSummary


## Properties

Name | Type
------------ | -------------
`registered` | number
`attended` | number
`no_show` | number
`cancelled` | number

## Example

```typescript
import type { EventParticipationSummary } from ''

// TODO: Update the object below with actual values
const example = {
  "registered": null,
  "attended": null,
  "no_show": null,
  "cancelled": null,
} satisfies EventParticipationSummary

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EventParticipationSummary
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


