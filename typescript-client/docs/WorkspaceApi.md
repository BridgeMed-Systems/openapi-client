# WorkspaceApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getOrganizationInsights**](WorkspaceApi.md#getorganizationinsights) | **GET** /v1/insights/organization | Read organization insights |
| [**getPlatformInsights**](WorkspaceApi.md#getplatforminsights) | **GET** /v1/insights/platform | Read platform insights |
| [**getRepsInsights**](WorkspaceApi.md#getrepsinsights) | **GET** /v1/insights/reps | Read reps insights |
| [**getVendorInsights**](WorkspaceApi.md#getvendorinsights) | **GET** /v1/insights/vendor | Read vendor insights |
| [**listWorkspaceActivity**](WorkspaceApi.md#listworkspaceactivity) | **GET** /v1/activity | List current workspace activity |
| [**listWorkspaceNotifications**](WorkspaceApi.md#listworkspacenotifications) | **GET** /v1/notifications | List personal workspace notifications |
| [**markWorkspaceNotificationRead**](WorkspaceApi.md#markworkspacenotificationread) | **POST** /v1/notifications/{id}/read | Mark a personal notification as read |
| [**searchWorkspace**](WorkspaceApi.md#searchworkspace) | **GET** /v1/search | Search visible workspace records |



## getOrganizationInsights

> WorkspaceInsights getOrganizationInsights()

Read organization insights

Existing permission-gated endpoint. Premium analytics capabilities are not granted to base V1 organization personas.

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { GetOrganizationInsightsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  try {
    const data = await api.getOrganizationInsights();
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

[**WorkspaceInsights**](WorkspaceInsights.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Read organization insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getPlatformInsights

> WorkspaceInsights getPlatformInsights()

Read platform insights

Existing permission-gated endpoint. Premium analytics capabilities are not granted to base V1 organization personas.

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { GetPlatformInsightsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  try {
    const data = await api.getPlatformInsights();
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

[**WorkspaceInsights**](WorkspaceInsights.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Read platform insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getRepsInsights

> WorkspaceInsights getRepsInsights()

Read reps insights

Existing permission-gated endpoint. Premium analytics capabilities are not granted to base V1 organization personas.

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { GetRepsInsightsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  try {
    const data = await api.getRepsInsights();
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

[**WorkspaceInsights**](WorkspaceInsights.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Read reps insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getVendorInsights

> WorkspaceInsights getVendorInsights()

Read vendor insights

Existing permission-gated endpoint. Premium analytics capabilities are not granted to base V1 organization personas.

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { GetVendorInsightsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  try {
    const data = await api.getVendorInsights();
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

[**WorkspaceInsights**](WorkspaceInsights.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Read vendor insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWorkspaceActivity

> Array&lt;WorkspaceActivityItem&gt; listWorkspaceActivity(limit)

List current workspace activity

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { ListWorkspaceActivityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  const body = {
    // number | Defaults to 12 and clamps to 5–20. (optional)
    limit: 56,
  } satisfies ListWorkspaceActivityRequest;

  try {
    const data = await api.listWorkspaceActivity(body);
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
| **limit** | `number` | Defaults to 12 and clamps to 5–20. | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;WorkspaceActivityItem&gt;**](WorkspaceActivityItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List current workspace activity |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWorkspaceNotifications

> Array&lt;WorkspaceNotification&gt; listWorkspaceNotifications(limit)

List personal workspace notifications

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { ListWorkspaceNotificationsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  const body = {
    // number | Defaults to 12 and clamps to 5–20. (optional)
    limit: 56,
  } satisfies ListWorkspaceNotificationsRequest;

  try {
    const data = await api.listWorkspaceNotifications(body);
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
| **limit** | `number` | Defaults to 12 and clamps to 5–20. | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;WorkspaceNotification&gt;**](WorkspaceNotification.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List personal workspace notifications |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## markWorkspaceNotificationRead

> NotificationReadResult markWorkspaceNotificationRead(id)

Mark a personal notification as read

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { MarkWorkspaceNotificationReadRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  const body = {
    // string
    id: id_example,
  } satisfies MarkWorkspaceNotificationReadRequest;

  try {
    const data = await api.markWorkspaceNotificationRead(body);
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

[**NotificationReadResult**](NotificationReadResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Mark a personal notification as read |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## searchWorkspace

> WorkspaceSearchResponse searchWorkspace(q, types, limit)

Search visible workspace records

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { SearchWorkspaceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string | Comma-separated products, content, reps, organizations, webinars, training. Unknown types are ignored. (optional)
    types: types_example,
    // number | Per group; defaults to 6 and clamps to 3–10. (optional)
    limit: 56,
  } satisfies SearchWorkspaceRequest;

  try {
    const data = await api.searchWorkspace(body);
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
| **types** | `string` | Comma-separated products, content, reps, organizations, webinars, training. Unknown types are ignored. | [Optional] [Defaults to `undefined`] |
| **limit** | `number` | Per group; defaults to 6 and clamps to 3–10. | [Optional] [Defaults to `undefined`] |

### Return type

[**WorkspaceSearchResponse**](WorkspaceSearchResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Search visible workspace records |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

