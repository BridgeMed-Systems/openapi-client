# WorkspaceApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getOrganizationInsights**](WorkspaceApi.md#getorganizationinsights) | **GET** /v1/insights/organization | Organization insights |
| [**getPlatformInsights**](WorkspaceApi.md#getplatforminsights) | **GET** /v1/insights/platform | Platform insights |
| [**getRepInsights**](WorkspaceApi.md#getrepinsights) | **GET** /v1/insights/reps | Rep insights |
| [**getVendorInsights**](WorkspaceApi.md#getvendorinsights) | **GET** /v1/insights/vendor | Vendor insights |
| [**listWorkspaceActivity**](WorkspaceApi.md#listworkspaceactivity) | **GET** /v1/activity | List workspace activity |
| [**listWorkspaceNotifications**](WorkspaceApi.md#listworkspacenotifications) | **GET** /v1/notifications | List in-app notifications |
| [**markWorkspaceNotificationRead**](WorkspaceApi.md#markworkspacenotificationread) | **POST** /v1/notifications/{id}/read | Mark notification read |



## getOrganizationInsights

> InsightsResponse getOrganizationInsights()

Organization insights

Hospital or organization scoped zero-PHI operational metrics and highlights for product/content/training engagement.

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

[**InsightsResponse**](InsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Organization insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getPlatformInsights

> InsightsResponse getPlatformInsights()

Platform insights

Platform-scoped zero-PHI operational metrics and highlights across tenants. Requires platform insights permission.

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

[**InsightsResponse**](InsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Platform insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getRepInsights

> InsightsResponse getRepInsights()

Rep insights

Representative-scoped zero-PHI operational metrics and highlights for assigned product/content/training engagement.

### Example

```ts
import {
  Configuration,
  WorkspaceApi,
} from '';
import type { GetRepInsightsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new WorkspaceApi(config);

  try {
    const data = await api.getRepInsights();
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

[**InsightsResponse**](InsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rep insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getVendorInsights

> InsightsResponse getVendorInsights()

Vendor insights

Vendor-scoped zero-PHI operational metrics and highlights for product/content/training engagement.

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

[**InsightsResponse**](InsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Vendor insights |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWorkspaceActivity

> Array&lt;ActivityItem&gt; listWorkspaceActivity(limit)

List workspace activity

Returns zero-PHI operational activity visible to the authenticated caller. Items use opaque resource identifiers and product/vendor workflow labels only; no patient, case, or schedule context is returned.

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
    // number (optional)
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
| **limit** | `number` |  | [Optional] [Defaults to `25`] |

### Return type

[**Array&lt;ActivityItem&gt;**](ActivityItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity items |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listWorkspaceNotifications

> Array&lt;NotificationItem&gt; listWorkspaceNotifications(limit)

List in-app notifications

Returns in-app BridgeMed workflow notifications for the authenticated caller. External email/message delivery is outside this endpoint and remains separately gated.

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
    // number (optional)
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
| **limit** | `number` |  | [Optional] [Defaults to `25`] |

### Return type

[**Array&lt;NotificationItem&gt;**](NotificationItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification items |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## markWorkspaceNotificationRead

> SimpleOKResponse markWorkspaceNotificationRead(id)

Mark notification read

Marks one authenticated-caller notification as read. The server scopes ownership by caller subject and does not expose another user\&#39;s notification content.

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
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
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

[**SimpleOKResponse**](SimpleOKResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification marked read |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)
