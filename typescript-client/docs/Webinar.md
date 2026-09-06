
# Webinar


## Properties

Name | Type
------------ | -------------
`delivery_mode` | string
`external_join_url` | string
`capacity` | number
`id` | string
`organization_id` | string
`host_user_id` | string
`title` | string
`description` | string
`starts_at` | Date
`ends_at` | Date
`status` | [WebinarStatus](WebinarStatus.md)
`started_at` | Date
`ended_at` | Date
`room_key` | string
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { Webinar } from ''

// TODO: Update the object below with actual values
const example = {
  "delivery_mode": null,
  "external_join_url": null,
  "capacity": null,
  "id": null,
  "organization_id": null,
  "host_user_id": null,
  "title": null,
  "description": null,
  "starts_at": null,
  "ends_at": null,
  "status": null,
  "started_at": null,
  "ended_at": null,
  "room_key": null,
  "date_added": null,
  "date_updated": null,
} satisfies Webinar

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Webinar
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


