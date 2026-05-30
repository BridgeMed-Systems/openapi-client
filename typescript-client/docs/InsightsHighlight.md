
# InsightsHighlight


## Properties

Name | Type
------------ | -------------
`key` | string
`title` | string
`subtitle` | string
`value` | string
`to` | string

## Example

```typescript
import type { InsightsHighlight } from ''

// TODO: Update the object below with actual values
const example = {
  "key": content_engagement,
  "title": Product content engagement increased,
  "subtitle": Organization-level activity only; no patient or case context,
  "value": +8%,
  "to": /insights/vendor,
} satisfies InsightsHighlight

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as InsightsHighlight
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
