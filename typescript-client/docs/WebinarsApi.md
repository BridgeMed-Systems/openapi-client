# WebinarsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWebinar**](WebinarsApi.md#createwebinaroperation) | **POST** /v1/webinars/ | Create webinar |
| [**createWebinarQnA**](WebinarsApi.md#createwebinarqnaoperation) | **POST** /v1/webinars/{id}/qna | Create webinar Q&amp;A item |
| [**endWebinar**](WebinarsApi.md#endwebinar) | **POST** /v1/webinars/{id}/end | End webinar |
| [**getWebinar**](WebinarsApi.md#getwebinar) | **GET** /v1/webinars/{id} | Get webinar |
| [**joinWebinar**](WebinarsApi.md#joinwebinaroperation) | **POST** /v1/webinars/{id}/join | Join webinar |
| [**listWebinarQnA**](WebinarsApi.md#listwebinarqna) | **GET** /v1/webinars/{id}/qna | List webinar Q&amp;A items |
| [**listWebinars**](WebinarsApi.md#listwebinars) | **GET** /v1/webinars/ | List webinars |
| [**signalWebinar**](WebinarsApi.md#signalwebinar) | **GET** /v1/webinars/{id}/signal | WebRTC signaling websocket endpoint |
| [**startWebinar**](WebinarsApi.md#startwebinar) | **POST** /v1/webinars/{id}/start | Start webinar |
| [**updateWebinar**](WebinarsApi.md#updatewebinaroperation) | **PATCH** /v1/webinars/{id} | Update webinar |
| [**updateWebinarQnA**](WebinarsApi.md#updatewebinarqnaoperation) | **PATCH** /v1/webinars/{id}/qna/{itemID} | Moderate webinar Q&amp;A item |



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

