
# VendorBillingSummary


## Properties

Name | Type
------------ | -------------
`organization_id` | string
`organization_name` | string
`access_mode` | string
`status` | string
`plan_key` | string
`interval` | string
`paid_through` | Date
`grace_until` | Date
`cancel_at_period_end` | boolean
`needs_review` | boolean
`can_checkout` | boolean
`can_open_portal` | boolean
`last_reconciled_at` | Date

## Example

```typescript
import type { VendorBillingSummary } from ''

// TODO: Update the object below with actual values
const example = {
  "organization_id": null,
  "organization_name": null,
  "access_mode": null,
  "status": null,
  "plan_key": null,
  "interval": null,
  "paid_through": null,
  "grace_until": null,
  "cancel_at_period_end": null,
  "needs_review": null,
  "can_checkout": null,
  "can_open_portal": null,
  "last_reconciled_at": null,
} satisfies VendorBillingSummary

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VendorBillingSummary
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


