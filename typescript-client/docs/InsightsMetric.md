
# InsightsMetric


## Properties

Name | Type
------------ | -------------
`key` | string
`label` | string
`value` | string
`tone` | string

## Example

```typescript
import type { InsightsMetric } from ''

// TODO: Update the object below with actual values
const example = {
  "key": training_requests_open,
  "label": Open training requests,
  "value": 12,
  "tone": info,
} satisfies InsightsMetric

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as InsightsMetric
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
