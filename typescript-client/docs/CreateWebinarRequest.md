
# CreateWebinarRequest


## Properties

Name | Type
------------ | -------------
`delivery_mode` | string
`external_join_url` | string
`capacity` | number
`organization_id` | string
`title` | string
`description` | string
`starts_at` | Date
`ends_at` | Date

## Example

```typescript
import type { CreateWebinarRequest } from ''

// TODO: Update the object below with actual values
const example = {
  "delivery_mode": null,
  "external_join_url": null,
  "capacity": null,
  "organization_id": null,
  "title": null,
  "description": null,
  "starts_at": null,
  "ends_at": null,
} satisfies CreateWebinarRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateWebinarRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


