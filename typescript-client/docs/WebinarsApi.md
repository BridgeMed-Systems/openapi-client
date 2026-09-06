# WebinarsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelWebinar**](WebinarsApi.md#cancelwebinar) | **POST** /v1/webinars/{id}/cancel | Cancel webinar |
| [**createWebinar**](WebinarsApi.md#createwebinaroperation) | **POST** /v1/webinars/ | Create webinar |
| [**createWebinarQnA**](WebinarsApi.md#createwebinarqnaoperation) | **POST** /v1/webinars/{id}/qna | Create webinar Q&amp;A item |
| [**endWebinar**](WebinarsApi.md#endwebinar) | **POST** /v1/webinars/{id}/end | End webinar |
| [**getHospitalWebinarAvailability**](WebinarsApi.md#gethospitalwebinaravailability) | **GET** /v1/webinars/{id}/availability | Read your hospital availability for an event |
| [**getWebinar**](WebinarsApi.md#getwebinar) | **GET** /v1/webinars/{id} | Get webinar |
| [**getWebinarAudience**](WebinarsApi.md#getwebinaraudience) | **GET** /v1/webinars/{id}/audience | List eligible hospitals and current event publication |
| [**joinWebinar**](WebinarsApi.md#joinwebinaroperation) | **POST** /v1/webinars/{id}/join | Join webinar |
| [**listWebinarQnA**](WebinarsApi.md#listwebinarqna) | **GET** /v1/webinars/{id}/qna | List webinar Q&amp;A items |
| [**listWebinars**](WebinarsApi.md#listwebinars) | **GET** /v1/webinars/ | List webinars |
| [**publishWebinarAudience**](WebinarsApi.md#publishwebinaraudience) | **PUT** /v1/webinars/{id}/audience/{organizationID} | Publish or withdraw a vendor event for one hospital |
| [**setHospitalWebinarAvailability**](WebinarsApi.md#sethospitalwebinaravailability) | **PUT** /v1/webinars/{id}/availability | Enable or disable event access for your hospital |
| [**signalWebinar**](WebinarsApi.md#signalwebinar) | **GET** /v1/webinars/{id}/signal | WebRTC signaling websocket endpoint |
| [**startWebinar**](WebinarsApi.md#startwebinar) | **POST** /v1/webinars/{id}/start | Start webinar |
| [**updateWebinar**](WebinarsApi.md#updatewebinaroperation) | **PATCH** /v1/webinars/{id} | Update webinar |
| [**updateWebinarQnA**](WebinarsApi.md#updatewebinarqnaoperation) | **PATCH** /v1/webinars/{id}/qna/{itemID} | Moderate webinar Q&amp;A item |



## cancelWebinar

> Webinar cancelWebinar(id)

Cancel webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { CancelWebinarRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CancelWebinarRequest;

  try {
    const data = await api.cancelWebinar(body);
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

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar cancelled |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createWebinar

> Webinar createWebinar(createWebinarRequest)

Create webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { CreateWebinarOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // CreateWebinarRequest
    createWebinarRequest: ...,
  } satisfies CreateWebinarOperationRequest;

  try {
    const data = await api.createWebinar(body);
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
| **createWebinarRequest** | [CreateWebinarRequest](CreateWebinarRequest.md) |  | |

### Return type

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Webinar created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createWebinarQnA

> WebinarQnAItem createWebinarQnA(id, createWebinarQnARequest)

Create webinar Q&amp;A item

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { CreateWebinarQnAOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateWebinarQnARequest
    createWebinarQnARequest: ...,
  } satisfies CreateWebinarQnAOperationRequest;

  try {
    const data = await api.createWebinarQnA(body);
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
| **createWebinarQnARequest** | [CreateWebinarQnARequest](CreateWebinarQnARequest.md) |  | |

### Return type

[**WebinarQnAItem**](WebinarQnAItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Q&amp;A item created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## endWebinar

> Webinar endWebinar(id)

End webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { EndWebinarRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies EndWebinarRequest;

  try {
    const data = await api.endWebinar(body);
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

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar ended |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getHospitalWebinarAvailability

> EventAvailability getHospitalWebinarAvailability(id)

Read your hospital availability for an event

Vendor hosts and authorized company managers choose partner hospitals explicitly. Hospital administrators control access for their own staff. Withdrawing access preserves private participation history and sends cancellation updates to calendar subscriptions.

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { GetHospitalWebinarAvailabilityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetHospitalWebinarAvailabilityRequest;

  try {
    const data = await api.getHospitalWebinarAvailability(body);
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

[**EventAvailability**](EventAvailability.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current event availability |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getWebinar

> Webinar getWebinar(id)

Get webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { GetWebinarRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetWebinarRequest;

  try {
    const data = await api.getWebinar(body);
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

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getWebinarAudience

> Array&lt;AudienceHospital&gt; getWebinarAudience(id)

List eligible hospitals and current event publication

Vendor hosts and authorized company managers choose partner hospitals explicitly. Hospital administrators control access for their own staff. Withdrawing access preserves private participation history and sends cancellation updates to calendar subscriptions.

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { GetWebinarAudienceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetWebinarAudienceRequest;

  try {
    const data = await api.getWebinarAudience(body);
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

[**Array&lt;AudienceHospital&gt;**](AudienceHospital.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current event availability |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## joinWebinar

> WebinarJoinResult joinWebinar(id, joinWebinarRequest)

Join webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { JoinWebinarOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // JoinWebinarRequest (optional)
    joinWebinarRequest: ...,
  } satisfies JoinWebinarOperationRequest;

  try {
    const data = await api.joinWebinar(body);
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
| **joinWebinarRequest** | [JoinWebinarRequest](JoinWebinarRequest.md) |  | [Optional] |

### Return type

[**WebinarJoinResult**](WebinarJoinResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Join token issued |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Room capacity reached or admission revoked |  -  |
| **500** | Internal server error |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWebinarQnA

> Array&lt;WebinarQnAItem&gt; listWebinarQnA(id)

List webinar Q&amp;A items

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { ListWebinarQnARequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListWebinarQnARequest;

  try {
    const data = await api.listWebinarQnA(body);
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

[**Array&lt;WebinarQnAItem&gt;**](WebinarQnAItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar Q&amp;A items |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWebinars

> Array&lt;Webinar&gt; listWebinars(organizationId, hostUserId, statuses, start, end)

List webinars

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { ListWebinarsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    hostUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string | Comma-separated webinar statuses (optional)
    statuses: statuses_example,
    // Date (optional)
    start: 2013-10-20T19:20:30+01:00,
    // Date (optional)
    end: 2013-10-20T19:20:30+01:00,
  } satisfies ListWebinarsRequest;

  try {
    const data = await api.listWebinars(body);
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
| **hostUserId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **statuses** | `string` | Comma-separated webinar statuses | [Optional] [Defaults to `undefined`] |
| **start** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **end** | `Date` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;Webinar&gt;**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinars |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publishWebinarAudience

> publishWebinarAudience(id, organizationID, eventPublication)

Publish or withdraw a vendor event for one hospital

Vendor hosts and authorized company managers choose partner hospitals explicitly. Hospital administrators control access for their own staff. Withdrawing access preserves private participation history and sends cancellation updates to calendar subscriptions.

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { PublishWebinarAudienceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    organizationID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // EventPublication
    eventPublication: ...,
  } satisfies PublishWebinarAudienceRequest;

  try {
    const data = await api.publishWebinarAudience(body);
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
| **organizationID** | `string` |  | [Defaults to `undefined`] |
| **eventPublication** | [EventPublication](EventPublication.md) |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Event availability updated or already in the requested state |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## setHospitalWebinarAvailability

> setHospitalWebinarAvailability(id, eventAvailability)

Enable or disable event access for your hospital

Vendor hosts and authorized company managers choose partner hospitals explicitly. Hospital administrators control access for their own staff. Withdrawing access preserves private participation history and sends cancellation updates to calendar subscriptions.

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { SetHospitalWebinarAvailabilityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // EventAvailability
    eventAvailability: ...,
  } satisfies SetHospitalWebinarAvailabilityRequest;

  try {
    const data = await api.setHospitalWebinarAvailability(body);
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
| **eventAvailability** | [EventAvailability](EventAvailability.md) |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Event availability updated or already in the requested state |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## signalWebinar

> signalWebinar(id, participantToken)

WebRTC signaling websocket endpoint

Requires a current authenticated browser session and a participant token for that same user and room.

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { SignalWebinarRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    participantToken: participantToken_example,
  } satisfies SignalWebinarRequest;

  try {
    const data = await api.signalWebinar(body);
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
| **participantToken** | `string` |  | [Defaults to `undefined`] |

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
| **101** | Switching protocols to websocket |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **410** | Legacy transport retired. Rejoin through the current LiveKit flow. |  -  |
| **503** | Signaling unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startWebinar

> Webinar startWebinar(id)

Start webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { StartWebinarRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies StartWebinarRequest;

  try {
    const data = await api.startWebinar(body);
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

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar started |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateWebinar

> Webinar updateWebinar(id, updateWebinarRequest)

Update webinar

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { UpdateWebinarOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateWebinarRequest
    updateWebinarRequest: ...,
  } satisfies UpdateWebinarOperationRequest;

  try {
    const data = await api.updateWebinar(body);
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
| **updateWebinarRequest** | [UpdateWebinarRequest](UpdateWebinarRequest.md) |  | |

### Return type

[**Webinar**](Webinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Webinar updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateWebinarQnA

> WebinarQnAItem updateWebinarQnA(id, itemID, updateWebinarQnARequest)

Moderate webinar Q&amp;A item

### Example

```ts
import {
  Configuration,
  WebinarsApi,
} from '';
import type { UpdateWebinarQnAOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WebinarsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    itemID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateWebinarQnARequest
    updateWebinarQnARequest: ...,
  } satisfies UpdateWebinarQnAOperationRequest;

  try {
    const data = await api.updateWebinarQnA(body);
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
| **itemID** | `string` |  | [Defaults to `undefined`] |
| **updateWebinarQnARequest** | [UpdateWebinarQnARequest](UpdateWebinarQnARequest.md) |  | |

### Return type

[**WebinarQnAItem**](WebinarQnAItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Q&amp;A item updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

