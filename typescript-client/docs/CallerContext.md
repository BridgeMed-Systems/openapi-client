
# CallerContext


## Properties

Name | Type
------------ | -------------
`persona` | string
`tenant_name` | string
`tenant_org_type` | string
`experience_tier` | string
`available_workspaces` | Array&lt;string&gt;
`subject` | string
`tenant_id` | string
`roles` | Array&lt;string&gt;
`permissions` | Array&lt;string&gt;
`claims` | { [key: string]: any; }

## Example

```typescript
import type { CallerContext } from ''

// TODO: Update the object below with actual values
const example = {
  "persona": null,
  "tenant_name": null,
  "tenant_org_type": null,
  "experience_tier": null,
  "available_workspaces": null,
  "subject": null,
  "tenant_id": null,
  "roles": null,
  "permissions": null,
  "claims": null,
} satisfies CallerContext

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CallerContext
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


