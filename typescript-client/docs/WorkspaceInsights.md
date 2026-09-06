
# WorkspaceInsights


## Properties

Name | Type
------------ | -------------
`scope` | string
`title` | string
`subtitle` | string
`metrics` | [Array&lt;WorkspaceInsightMetric&gt;](WorkspaceInsightMetric.md)
`highlights` | [Array&lt;WorkspaceInsightHighlight&gt;](WorkspaceInsightHighlight.md)
`recent_activity` | [Array&lt;WorkspaceActivityItem&gt;](WorkspaceActivityItem.md)

## Example

```typescript
import type { WorkspaceInsights } from ''

// TODO: Update the object below with actual values
const example = {
  "scope": null,
  "title": null,
  "subtitle": null,
  "metrics": null,
  "highlights": null,
  "recent_activity": null,
} satisfies WorkspaceInsights

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkspaceInsights
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


