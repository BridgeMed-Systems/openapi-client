# TrainingApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelMyTrainingSessionRegistration**](TrainingApi.md#cancelmytrainingsessionregistration) | **DELETE** /v1/training/sessions/{id}/registrations/me | Cancel my session registration |
| [**cancelTrainingSession**](TrainingApi.md#canceltrainingsession) | **POST** /v1/training/sessions/{id}/cancel | Cancel training session |
| [**completeTrainingSession**](TrainingApi.md#completetrainingsession) | **POST** /v1/training/sessions/{id}/complete | Complete training session |
| [**completeTrainingSessionMaterialUpload**](TrainingApi.md#completetrainingsessionmaterialupload) | **POST** /v1/training/sessions/{id}/materials/{materialID}/upload-complete | Finalize training session material upload |
| [**createTrainingRequest**](TrainingApi.md#createtrainingrequest) | **POST** /v1/training/requests/ | Create training request |
| [**createTrainingSession**](TrainingApi.md#createtrainingsessionoperation) | **POST** /v1/training/sessions/ | Create training session from request |
| [**createTrainingSessionMaterial**](TrainingApi.md#createtrainingsessionmaterialoperation) | **POST** /v1/training/sessions/{id}/materials | Create training session material |
| [**createTrainingSessionRegistration**](TrainingApi.md#createtrainingsessionregistrationoperation) | **POST** /v1/training/sessions/{id}/registrations | Register attendee for training session |
| [**deleteTrainingSessionMaterial**](TrainingApi.md#deletetrainingsessionmaterial) | **DELETE** /v1/training/sessions/{id}/materials/{materialID} | Delete training session material |
| [**downloadTrainingSessionMaterial**](TrainingApi.md#downloadtrainingsessionmaterial) | **GET** /v1/training/sessions/{id}/materials/{materialID}/download | Download training session material |
| [**getTrainingSession**](TrainingApi.md#gettrainingsession) | **GET** /v1/training/sessions/{id} | Get training session |
| [**joinTrainingSession**](TrainingApi.md#jointrainingsession) | **POST** /v1/training/sessions/{id}/join | Join training session |
| [**listTrainingRequests**](TrainingApi.md#listtrainingrequests) | **GET** /v1/training/requests/ | List training requests |
| [**listTrainingSessionMaterials**](TrainingApi.md#listtrainingsessionmaterials) | **GET** /v1/training/sessions/{id}/materials | List training session materials |
| [**listTrainingSessionRegistrations**](TrainingApi.md#listtrainingsessionregistrations) | **GET** /v1/training/sessions/{id}/registrations | List training session registrations |
| [**listTrainingSessions**](TrainingApi.md#listtrainingsessions) | **GET** /v1/training/sessions/ | List training sessions |
| [**startTrainingSession**](TrainingApi.md#starttrainingsession) | **POST** /v1/training/sessions/{id}/start | Start training session |
| [**updateTrainingRequestStatus**](TrainingApi.md#updatetrainingrequeststatusoperation) | **PATCH** /v1/training/requests/{id} | Update training request status |
| [**updateTrainingSession**](TrainingApi.md#updatetrainingsessionoperation) | **PATCH** /v1/training/sessions/{id} | Update training session |
| [**updateTrainingSessionMaterial**](TrainingApi.md#updatetrainingsessionmaterialoperation) | **PATCH** /v1/training/sessions/{id}/materials/{materialID} | Update training session material |
| [**updateTrainingSessionRegistration**](TrainingApi.md#updatetrainingsessionregistrationoperation) | **PATCH** /v1/training/sessions/{id}/registrations/{userID} | Update training session registration |
| [**uploadTrainingSessionMaterialContent**](TrainingApi.md#uploadtrainingsessionmaterialcontent) | **PUT** /v1/training/sessions/{id}/materials/{materialID}/content | Upload training session material content |



## cancelMyTrainingSessionRegistration

> cancelMyTrainingSessionRegistration(id)

Cancel my session registration

Idempotently cancels a pending personal registration. Attendance already recorded must be corrected by a hospital administrator.

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CancelMyTrainingSessionRegistrationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CancelMyTrainingSessionRegistrationRequest;

  try {
    const data = await api.cancelMyTrainingSessionRegistration(body);
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

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Personal registration is cancelled or absent |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **400** | Validation or request shape error |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## cancelTrainingSession

> TrainingSession cancelTrainingSession(id)

Cancel training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CancelTrainingSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CancelTrainingSessionRequest;

  try {
    const data = await api.cancelTrainingSession(body);
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

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session cancelled |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## completeTrainingSession

> TrainingSession completeTrainingSession(id)

Complete training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CompleteTrainingSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CompleteTrainingSessionRequest;

  try {
    const data = await api.completeTrainingSession(body);
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

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session completed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## completeTrainingSessionMaterialUpload

> TrainingSessionMaterial completeTrainingSessionMaterialUpload(id, materialID)

Finalize training session material upload

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CompleteTrainingSessionMaterialUploadRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    materialID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CompleteTrainingSessionMaterialUploadRequest;

  try {
    const data = await api.completeTrainingSessionMaterialUpload(body);
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
| **materialID** | `string` |  | [Defaults to `undefined`] |

### Return type

[**TrainingSessionMaterial**](TrainingSessionMaterial.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session material upload finalized |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createTrainingRequest

> TrainingRequest createTrainingRequest(createTrainingRequest)

Create training request

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CreateTrainingRequestRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // CreateTrainingRequest
    createTrainingRequest: ...,
  } satisfies CreateTrainingRequestRequest;

  try {
    const data = await api.createTrainingRequest(body);
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
| **createTrainingRequest** | [CreateTrainingRequest](CreateTrainingRequest.md) |  | |

### Return type

[**TrainingRequest**](TrainingRequest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Training request created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createTrainingSession

> TrainingSession createTrainingSession(createTrainingSessionRequest)

Create training session from request

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CreateTrainingSessionOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // CreateTrainingSessionRequest
    createTrainingSessionRequest: ...,
  } satisfies CreateTrainingSessionOperationRequest;

  try {
    const data = await api.createTrainingSession(body);
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
| **createTrainingSessionRequest** | [CreateTrainingSessionRequest](CreateTrainingSessionRequest.md) |  | |

### Return type

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Training session created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createTrainingSessionMaterial

> TrainingSessionMaterial createTrainingSessionMaterial(id, createTrainingSessionMaterialRequest)

Create training session material

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CreateTrainingSessionMaterialOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateTrainingSessionMaterialRequest
    createTrainingSessionMaterialRequest: ...,
  } satisfies CreateTrainingSessionMaterialOperationRequest;

  try {
    const data = await api.createTrainingSessionMaterial(body);
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
| **createTrainingSessionMaterialRequest** | [CreateTrainingSessionMaterialRequest](CreateTrainingSessionMaterialRequest.md) |  | |

### Return type

[**TrainingSessionMaterial**](TrainingSessionMaterial.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Training session material created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createTrainingSessionRegistration

> TrainingSessionRegistration createTrainingSessionRegistration(id, createTrainingSessionRegistrationRequest)

Register attendee for training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { CreateTrainingSessionRegistrationOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateTrainingSessionRegistrationRequest (optional)
    createTrainingSessionRegistrationRequest: ...,
  } satisfies CreateTrainingSessionRegistrationOperationRequest;

  try {
    const data = await api.createTrainingSessionRegistration(body);
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
| **createTrainingSessionRegistrationRequest** | [CreateTrainingSessionRegistrationRequest](CreateTrainingSessionRegistrationRequest.md) |  | [Optional] |

### Return type

[**TrainingSessionRegistration**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Training session registration created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteTrainingSessionMaterial

> deleteTrainingSessionMaterial(id, materialID)

Delete training session material

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { DeleteTrainingSessionMaterialRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    materialID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeleteTrainingSessionMaterialRequest;

  try {
    const data = await api.deleteTrainingSessionMaterial(body);
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
| **materialID** | `string` |  | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Training session material removed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## downloadTrainingSessionMaterial

> Blob downloadTrainingSessionMaterial(id, materialID)

Download training session material

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { DownloadTrainingSessionMaterialRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    materialID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DownloadTrainingSessionMaterialRequest;

  try {
    const data = await api.downloadTrainingSessionMaterial(body);
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
| **materialID** | `string` |  | [Defaults to `undefined`] |

### Return type

**Blob**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/octet-stream`, `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session material binary |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getTrainingSession

> TrainingSession getTrainingSession(id)

Get training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { GetTrainingSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetTrainingSessionRequest;

  try {
    const data = await api.getTrainingSession(body);
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

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## joinTrainingSession

> TrainingSessionJoinResult joinTrainingSession(id)

Join training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { JoinTrainingSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies JoinTrainingSessionRequest;

  try {
    const data = await api.joinTrainingSession(body);
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

[**TrainingSessionJoinResult**](TrainingSessionJoinResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session join payload |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Room capacity reached or admission revoked |  -  |
| **500** | Internal server error |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listTrainingRequests

> Array&lt;TrainingRequest&gt; listTrainingRequests(organizationId, submittedByUserId, assignedUserId, statuses, scope)

List training requests

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { ListTrainingRequestsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    submittedByUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    assignedUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string | Comma-separated training request statuses (optional)
    statuses: statuses_example,
    // 'assigned_products' (optional)
    scope: scope_example,
  } satisfies ListTrainingRequestsRequest;

  try {
    const data = await api.listTrainingRequests(body);
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
| **organizationId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **submittedByUserId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **assignedUserId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **statuses** | `string` | Comma-separated training request statuses | [Optional] [Defaults to `undefined`] |
| **scope** | `assigned_products` |  | [Optional] [Defaults to `undefined`] [Enum: assigned_products] |

### Return type

[**Array&lt;TrainingRequest&gt;**](TrainingRequest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training requests |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listTrainingSessionMaterials

> Array&lt;TrainingSessionMaterial&gt; listTrainingSessionMaterials(id)

List training session materials

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { ListTrainingSessionMaterialsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListTrainingSessionMaterialsRequest;

  try {
    const data = await api.listTrainingSessionMaterials(body);
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

[**Array&lt;TrainingSessionMaterial&gt;**](TrainingSessionMaterial.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session materials |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listTrainingSessionRegistrations

> Array&lt;TrainingSessionRegistration&gt; listTrainingSessionRegistrations(id)

List training session registrations

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { ListTrainingSessionRegistrationsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListTrainingSessionRegistrationsRequest;

  try {
    const data = await api.listTrainingSessionRegistrations(body);
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

[**Array&lt;TrainingSessionRegistration&gt;**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session registrations |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listTrainingSessions

> Array&lt;TrainingSession&gt; listTrainingSessions(statuses, sourceRequestId)

List training sessions

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { ListTrainingSessionsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string | Comma-separated training session statuses (optional)
    statuses: statuses_example,
    // string (optional)
    sourceRequestId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListTrainingSessionsRequest;

  try {
    const data = await api.listTrainingSessions(body);
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
| **statuses** | `string` | Comma-separated training session statuses | [Optional] [Defaults to `undefined`] |
| **sourceRequestId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;TrainingSession&gt;**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training sessions |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startTrainingSession

> TrainingSession startTrainingSession(id)

Start training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { StartTrainingSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies StartTrainingSessionRequest;

  try {
    const data = await api.startTrainingSession(body);
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

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session started |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateTrainingRequestStatus

> TrainingRequest updateTrainingRequestStatus(id, updateTrainingRequestStatusRequest)

Update training request status

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { UpdateTrainingRequestStatusOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateTrainingRequestStatusRequest
    updateTrainingRequestStatusRequest: ...,
  } satisfies UpdateTrainingRequestStatusOperationRequest;

  try {
    const data = await api.updateTrainingRequestStatus(body);
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
| **updateTrainingRequestStatusRequest** | [UpdateTrainingRequestStatusRequest](UpdateTrainingRequestStatusRequest.md) |  | |

### Return type

[**TrainingRequest**](TrainingRequest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training request updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateTrainingSession

> TrainingSession updateTrainingSession(id, updateTrainingSessionRequest)

Update training session

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { UpdateTrainingSessionOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateTrainingSessionRequest
    updateTrainingSessionRequest: ...,
  } satisfies UpdateTrainingSessionOperationRequest;

  try {
    const data = await api.updateTrainingSession(body);
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
| **updateTrainingSessionRequest** | [UpdateTrainingSessionRequest](UpdateTrainingSessionRequest.md) |  | |

### Return type

[**TrainingSession**](TrainingSession.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateTrainingSessionMaterial

> TrainingSessionMaterial updateTrainingSessionMaterial(id, materialID, updateTrainingSessionMaterialRequest)

Update training session material

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { UpdateTrainingSessionMaterialOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    materialID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateTrainingSessionMaterialRequest
    updateTrainingSessionMaterialRequest: ...,
  } satisfies UpdateTrainingSessionMaterialOperationRequest;

  try {
    const data = await api.updateTrainingSessionMaterial(body);
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
| **materialID** | `string` |  | [Defaults to `undefined`] |
| **updateTrainingSessionMaterialRequest** | [UpdateTrainingSessionMaterialRequest](UpdateTrainingSessionMaterialRequest.md) |  | |

### Return type

[**TrainingSessionMaterial**](TrainingSessionMaterial.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session material updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateTrainingSessionRegistration

> TrainingSessionRegistration updateTrainingSessionRegistration(id, userID, updateTrainingSessionRegistrationRequest)

Update training session registration

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { UpdateTrainingSessionRegistrationOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateTrainingSessionRegistrationRequest
    updateTrainingSessionRegistrationRequest: ...,
  } satisfies UpdateTrainingSessionRegistrationOperationRequest;

  try {
    const data = await api.updateTrainingSessionRegistration(body);
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
| **userID** | `string` |  | [Defaults to `undefined`] |
| **updateTrainingSessionRegistrationRequest** | [UpdateTrainingSessionRegistrationRequest](UpdateTrainingSessionRegistrationRequest.md) |  | |

### Return type

[**TrainingSessionRegistration**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Training session registration updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## uploadTrainingSessionMaterialContent

> uploadTrainingSessionMaterialContent(id, materialID, token, body)

Upload training session material content

### Example

```ts
import {
  Configuration,
  TrainingApi,
} from '';
import type { UploadTrainingSessionMaterialContentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new TrainingApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    materialID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    token: token_example,
    // Blob
    body: BINARY_DATA_HERE,
  } satisfies UploadTrainingSessionMaterialContentRequest;

  try {
    const data = await api.uploadTrainingSessionMaterialContent(body);
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
| **materialID** | `string` |  | [Defaults to `undefined`] |
| **token** | `string` |  | [Defaults to `undefined`] |
| **body** | `Blob` |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/octet-stream`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Training session material content uploaded |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

