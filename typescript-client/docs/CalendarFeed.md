
# CalendarFeed


## Properties

Name | Type
------------ | -------------
`id` | string
`owner_user_id` | string
`scope` | [CalendarFeedScope](CalendarFeedScope.md)
`organization_id` | string
`url` | string
`date_added` | Date
`date_rotated` | Date

## Example

```typescript
import type { CalendarFeed } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "owner_user_id": null,
  "scope": null,
  "organization_id": null,
  "url": null,
  "date_added": null,
  "date_rotated": null,
} satisfies CalendarFeed

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CalendarFeed
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


