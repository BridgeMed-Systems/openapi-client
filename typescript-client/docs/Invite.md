
# Invite


## Properties

Name | Type
------------ | -------------
`role_key` | string
`department_id` | string
`invited_by_user_id` | string
`id` | string
`email` | string
`first_name` | string
`last_name` | string
`phone_number` | string
`persona` | [UserPersona](UserPersona.md)
`organization_id` | string
`expires_at` | Date
`consumed_at` | Date
`consumed_by_user_id` | string
`date_added` | Date
`date_updated` | Date

## Example

```typescript
import type { Invite } from ''

// TODO: Update the object below with actual values
const example = {
  "role_key": null,
  "department_id": null,
  "invited_by_user_id": null,
  "id": null,
  "email": null,
  "first_name": null,
  "last_name": null,
  "phone_number": null,
  "persona": null,
  "organization_id": null,
  "expires_at": null,
  "consumed_at": null,
  "consumed_by_user_id": null,
  "date_added": null,
  "date_updated": null,
} satisfies Invite

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Invite
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


