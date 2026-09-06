# BillingApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getVendorBilling**](BillingApi.md#getvendorbilling) | **GET** /v1/billing | Read current organization billing |
| [**listVendorPlans**](BillingApi.md#listvendorplans) | **GET** /v1/vendor-plans | Read available organization prices |
| [**openVendorBillingPortal**](BillingApi.md#openvendorbillingportal) | **POST** /v1/billing/portal | Open hosted billing management and recovery |
| [**receiveStripeBillingWebhook**](BillingApi.md#receivestripebillingwebhook) | **POST** /billing/webhooks/stripe | Verify and durably capture a Stripe event |
| [**refreshVendorBilling**](BillingApi.md#refreshvendorbilling) | **POST** /v1/billing/refresh | Reconcile current organization subscription |
| [**startVendorCheckout**](BillingApi.md#startvendorcheckout) | **POST** /v1/billing/checkout | Start or recover hosted organization checkout |



## getVendorBilling

> VendorBillingSummary getVendorBilling()

Read current organization billing

Requires the current vendor organization administrator and billing.manage. No caller-supplied organization or customer is accepted.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { GetVendorBillingRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BillingApi(config);

  try {
    const data = await api.getVendorBilling();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**VendorBillingSummary**](VendorBillingSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current saved billing state |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listVendorPlans

> Array&lt;VendorPrice&gt; listVendorPlans()

Read available organization prices

Amounts and currencies come from configured Stripe prices. Provider IDs are private. Prices are cached for five minutes; checkout validates the current provider price again.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { ListVendorPlansRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new BillingApi();

  try {
    const data = await api.listVendorPlans();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Array&lt;VendorPrice&gt;**](VendorPrice.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Configured monthly and annual prices |  -  |
| **429** | Too many requests; Retry-After is 60 seconds |  -  |
| **503** | Prices or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## openVendorBillingPortal

> BillingHostedAction openVendorBillingPortal(body)

Open hosted billing management and recovery

Requires billing.manage and current vendor administrator access. Available after paid access lapses. The server selects the mapped customer and validated full or restricted recovery portal configuration.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { OpenVendorBillingPortalRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BillingApi(config);

  const body = {
    // object
    body: Object,
  } satisfies OpenVendorBillingPortalRequest;

  try {
    const data = await api.openVendorBillingPortal(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | `object` |  | |

### Return type

[**BillingHostedAction**](BillingHostedAction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Authenticated hosted portal URL |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **415** | JSON content type required |  -  |
| **429** | Too many organization billing mutations; Retry-After is 60 seconds |  -  |
| **500** | Internal server error |  -  |
| **503** | Provider or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## receiveStripeBillingWebhook

> receiveStripeBillingWebhook(stripeSignature, requestBody)

Verify and durably capture a Stripe event

The untouched body is limited to 1 MiB. Only valid signed events in the configured test/live mode are accepted; recognized events are acknowledged after durable idempotent capture. Signed unsupported event types are acknowledged without persistence.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { ReceiveStripeBillingWebhookRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new BillingApi();

  const body = {
    // string
    stripeSignature: stripeSignature_example,
    // { [key: string]: any; }
    requestBody: Object,
  } satisfies ReceiveStripeBillingWebhookRequest;

  try {
    const data = await api.receiveStripeBillingWebhook(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **stripeSignature** | `string` |  | [Defaults to `undefined`] |
| **requestBody** | `{ [key: string]: any; }` |  | |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Durably captured or authenticated unsupported event |  -  |
| **400** | Invalid signature, event or body size |  -  |
| **503** | Durable capture unavailable; Stripe should retry |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## refreshVendorBilling

> VendorBillingSummary refreshVendorBilling(body)

Reconcile current organization subscription

Requires billing.manage and current vendor administrator access. A return from hosted checkout is not proof of payment; reconciliation retrieves authoritative provider state.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { RefreshVendorBillingRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BillingApi(config);

  const body = {
    // object
    body: Object,
  } satisfies RefreshVendorBillingRequest;

  try {
    const data = await api.refreshVendorBilling(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **body** | `object` |  | |

### Return type

[**VendorBillingSummary**](VendorBillingSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reconciled billing state |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **415** | JSON content type required |  -  |
| **429** | Too many organization billing mutations; Retry-After is 60 seconds |  -  |
| **500** | Internal server error |  -  |
| **503** | Provider or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startVendorCheckout

> BillingHostedAction startVendorCheckout(vendorCheckoutInput)

Start or recover hosted organization checkout

Requires billing.manage and current vendor administrator access. Server-persisted operation identities provide idempotency. An unresolved checkout is recovered before a new one can be created. Existing subscriptions must be managed through the portal.

### Example

```ts
import {
  Configuration,
  BillingApi,
} from '';
import type { StartVendorCheckoutRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BillingApi(config);

  const body = {
    // VendorCheckoutInput
    vendorCheckoutInput: ...,
  } satisfies StartVendorCheckoutRequest;

  try {
    const data = await api.startVendorCheckout(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **vendorCheckoutInput** | [VendorCheckoutInput](VendorCheckoutInput.md) |  | |

### Return type

[**BillingHostedAction**](BillingHostedAction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Authenticated hosted checkout URL |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **415** | JSON content type required |  -  |
| **429** | Too many organization billing mutations; Retry-After is 60 seconds |  -  |
| **500** | Internal server error |  -  |
| **503** | Provider or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

