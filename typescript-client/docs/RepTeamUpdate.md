
# RepTeamUpdate


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

## Example

```typescript
import type { RepTeamUpdate } from ''

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
} satisfies RepTeamUpdate

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepTeamUpdate
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


