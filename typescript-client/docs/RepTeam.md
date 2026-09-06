
# RepTeam


## Properties

Name | Type
------------ | -------------
`members` | [Array&lt;RepTeamMember&gt;](RepTeamMember.md)
`products` | [Array&lt;RepTeamReference&gt;](RepTeamReference.md)
`accounts` | [Array&lt;RepTeamReference&gt;](RepTeamReference.md)

## Example

```typescript
import type { RepTeam } from ''

// TODO: Update the object below with actual values
const example = {
  "members": null,
  "products": null,
  "accounts": null,
} satisfies RepTeam

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RepTeam
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


