
# ActivityItem


## Properties

Name | Type
------------ | -------------
`id` | string
`type` | string
`title` | string
`subtitle` | string
`timestamp` | Date
`to` | string
`severity` | string

## Example

```typescript
import type { ActivityItem } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "type": training_request,
  "title": Training request updated,
  "subtitle": Product education workflow changed status,
  "timestamp": null,
  "to": /training/requests/11111111-1111-4111-8111-111111111111,
  "severity": info,
} satisfies ActivityItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ActivityItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
