
# VideoUploadInstructions


## Properties

Name | Type
------------ | -------------
`method` | string
`url` | string
`headers` | { [key: string]: string; }
`expires_at` | Date

## Example

```typescript
import type { VideoUploadInstructions } from ''

// TODO: Update the object below with actual values
const example = {
  "method": null,
  "url": null,
  "headers": null,
  "expires_at": null,
} satisfies VideoUploadInstructions

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoUploadInstructions
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


