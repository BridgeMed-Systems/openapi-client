
# WorkspaceNotification


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
import type { WorkspaceNotification } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "title": null,
  "subtitle": null,
  "created_at": null,
  "priority": null,
  "to": null,
  "read_at": null,
} satisfies WorkspaceNotification

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkspaceNotification
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


