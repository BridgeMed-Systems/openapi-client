
# InsightsResponse


## Properties

Name | Type
------------ | -------------
`scope` | string
`title` | string
`subtitle` | string
`metrics` | [Array&lt;InsightsMetric&gt;](InsightsMetric.md)
`highlights` | [Array&lt;InsightsHighlight&gt;](InsightsHighlight.md)
`recent_activity` | [Array&lt;ActivityItem&gt;](ActivityItem.md)

## Example

```typescript
import type { InsightsResponse } from ''

// TODO: Update the object below with actual values
const example = {
  "scope": vendor,
  "title": Vendor engagement insights,
  "subtitle": Product education and content activity; no patient, case, or schedule data,
  "metrics": null,
  "highlights": null,
  "recent_activity": null,
} satisfies InsightsResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as InsightsResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
