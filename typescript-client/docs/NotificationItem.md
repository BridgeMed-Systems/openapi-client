
# NotificationItem


## Properties

Name | Type
------------ | -------------
`id` | string
`title` | string
`subtitle` | string
`created_at` | Date
`priority` | string
`to` | string
`read_at` | Date

## Example

```typescript
import type { NotificationItem } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "title": Training request awaiting acknowledgment,
  "subtitle": Product education workflow update,
  "created_at": null,
  "priority": normal,
  "to": /notifications/11111111-1111-4111-8111-111111111111,
  "read_at": null,
} satisfies NotificationItem

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as NotificationItem
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
