# RepComplianceApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createRepComplianceRequirement**](RepComplianceApi.md#createrepcompliancerequirement) | **POST** /v1/rep-compliance/requirements | Assign an external education requirement to a supported representative |
| [**exportRepCompliance**](RepComplianceApi.md#exportrepcompliance) | **GET** /v1/rep-compliance/export.csv | Export filtered organization-owned rep compliance |
| [**getRepComplianceDetail**](RepComplianceApi.md#getrepcompliancedetail) | **GET** /v1/rep-compliance/requirements/{id} | Read a requirement and its retained external evidence history |
| [**listRepCompliancePeople**](RepComplianceApi.md#listrepcompliancepeople) | **GET** /v1/rep-compliance/people | Find representatives currently supporting this organization |
| [**listRepComplianceRequirements**](RepComplianceApi.md#listrepcompliancerequirements) | **GET** /v1/rep-compliance/requirements | List organization-owned external rep requirements |
| [**recordRepComplianceEvidence**](RepComplianceApi.md#recordrepcomplianceevidence) | **POST** /v1/rep-compliance/requirements/{id}/evidence | Record verified external completion and provider expiration |
| [**setRepComplianceRequirementEnabled**](RepComplianceApi.md#setrepcompliancerequirementenabled) | **PUT** /v1/rep-compliance/requirements/{id} | Enable or stop an external rep requirement |
| [**voidRepComplianceEvidence**](RepComplianceApi.md#voidrepcomplianceevidence) | **POST** /v1/rep-compliance/evidence/{id}/void | Void incorrect evidence without rewriting history |



## createRepComplianceRequirement

> RepComplianceRequirement createRepComplianceRequirement(idempotencyKey, repComplianceRequirementInput)

Assign an external education requirement to a supported representative

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { CreateRepComplianceRequirementRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RepComplianceRequirementInput
    repComplianceRequirementInput: ...,
  } satisfies CreateRepComplianceRequirementRequest;

  try {
    const data = await api.createRepComplianceRequirement(body);
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
| **idempotencyKey** | `string` |  | [Defaults to `undefined`] |
| **repComplianceRequirementInput** | [RepComplianceRequirementInput](RepComplianceRequirementInput.md) |  | |

### Return type

[**RepComplianceRequirement**](RepComplianceRequirement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## exportRepCompliance

> Blob exportRepCompliance(q, state, repUserId)

Export filtered organization-owned rep compliance

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { ExportRepComplianceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // '' | 'outstanding' | 'assigned' | 'completed' | 'overdue' | 'expired' | 'stopped' (optional)
    state: state_example,
    // string (optional)
    repUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ExportRepComplianceRequest;

  try {
    const data = await api.exportRepCompliance(body);
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
| **q** | `string` |  | [Optional] [Defaults to `undefined`] |
| **state** | ``, `outstanding`, `assigned`, `completed`, `overdue`, `expired`, `stopped` |  | [Optional] [Defaults to `undefined`] [Enum: , outstanding, assigned, completed, overdue, expired, stopped] |
| **repUserId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

**Blob**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/csv`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getRepComplianceDetail

> RepComplianceDetail getRepComplianceDetail(id)

Read a requirement and its retained external evidence history

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { GetRepComplianceDetailRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetRepComplianceDetailRequest;

  try {
    const data = await api.getRepComplianceDetail(body);
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
| **id** | `string` |  | [Defaults to `undefined`] |

### Return type

[**RepComplianceDetail**](RepComplianceDetail.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listRepCompliancePeople

> RepCompliancePersonPage listRepCompliancePeople(q, limit, offset)

Find representatives currently supporting this organization

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { ListRepCompliancePeopleRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListRepCompliancePeopleRequest;

  try {
    const data = await api.listRepCompliancePeople(body);
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
| **q** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**RepCompliancePersonPage**](RepCompliancePersonPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listRepComplianceRequirements

> RepComplianceRequirementPage listRepComplianceRequirements(q, state, repUserId, limit, offset)

List organization-owned external rep requirements

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { ListRepComplianceRequirementsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // '' | 'outstanding' | 'assigned' | 'completed' | 'overdue' | 'expired' | 'stopped' (optional)
    state: state_example,
    // string (optional)
    repUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListRepComplianceRequirementsRequest;

  try {
    const data = await api.listRepComplianceRequirements(body);
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
| **q** | `string` |  | [Optional] [Defaults to `undefined`] |
| **state** | ``, `outstanding`, `assigned`, `completed`, `overdue`, `expired`, `stopped` |  | [Optional] [Defaults to `undefined`] [Enum: , outstanding, assigned, completed, overdue, expired, stopped] |
| **repUserId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**RepComplianceRequirementPage**](RepComplianceRequirementPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## recordRepComplianceEvidence

> RepComplianceEvidence recordRepComplianceEvidence(id, idempotencyKey, repComplianceEvidenceInput)

Record verified external completion and provider expiration

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { RecordRepComplianceEvidenceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RepComplianceEvidenceInput
    repComplianceEvidenceInput: ...,
  } satisfies RecordRepComplianceEvidenceRequest;

  try {
    const data = await api.recordRepComplianceEvidence(body);
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
| **id** | `string` |  | [Defaults to `undefined`] |
| **idempotencyKey** | `string` |  | [Defaults to `undefined`] |
| **repComplianceEvidenceInput** | [RepComplianceEvidenceInput](RepComplianceEvidenceInput.md) |  | |

### Return type

[**RepComplianceEvidence**](RepComplianceEvidence.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## setRepComplianceRequirementEnabled

> RepComplianceRequirement setRepComplianceRequirementEnabled(id, repComplianceRequirementStatus)

Enable or stop an external rep requirement

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { SetRepComplianceRequirementEnabledRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RepComplianceRequirementStatus
    repComplianceRequirementStatus: ...,
  } satisfies SetRepComplianceRequirementEnabledRequest;

  try {
    const data = await api.setRepComplianceRequirementEnabled(body);
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
| **id** | `string` |  | [Defaults to `undefined`] |
| **repComplianceRequirementStatus** | [RepComplianceRequirementStatus](RepComplianceRequirementStatus.md) |  | |

### Return type

[**RepComplianceRequirement**](RepComplianceRequirement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## voidRepComplianceEvidence

> RepComplianceEvidence voidRepComplianceEvidence(id, repComplianceVoidRequest)

Void incorrect evidence without rewriting history

Hospital-owned and vendor-owned records remain separate. Field reps, regional managers, and human platform administrators cannot access these records.

### Example

```ts
import {
  Configuration,
  RepComplianceApi,
} from '';
import type { VoidRepComplianceEvidenceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepComplianceApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RepComplianceVoidRequest
    repComplianceVoidRequest: ...,
  } satisfies VoidRepComplianceEvidenceRequest;

  try {
    const data = await api.voidRepComplianceEvidence(body);
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
| **id** | `string` |  | [Defaults to `undefined`] |
| **repComplianceVoidRequest** | [RepComplianceVoidRequest](RepComplianceVoidRequest.md) |  | |

### Return type

[**RepComplianceEvidence**](RepComplianceEvidence.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital or vendor compliance permission required |  -  |
| **404** | Record unavailable in this organization |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

