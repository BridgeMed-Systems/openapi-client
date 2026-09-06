
# RepTeamMember


## Properties

Name | Type
------------ | -------------
`first_name` | string
`last_name` | string
`email` | string
`phone_number` | string
`title` | string
`role` | string
`manager_user_id` | string
`revision` | number
`product_ids` | Set&lt;string&gt;
`account_ids` | Set&lt;string&gt;
`user_id` | string

## Example

```typescript
import type { RepTeamMember } from ''

// TODO: Update the object below with actual values
const example = {
  "first_name": null,
  "last_name": null,
  "email": null,
  "phone_number": null,
  "title": null,
  "role": null,
  "manager_user_id": null,
  "revision": null,
  "product_ids": null,
  "account_ids": null,
  "user_id": null,
} satisfies RepTeamMember

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepTeamMember
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


