# AuthApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createSession**](AuthApi.md#createsessionoperation) | **POST** /v1/auth/session | Start session |
| [**getMe**](AuthApi.md#getme) | **GET** /v1/auth/me | Current caller context |
| [**listOrganizationAccess**](AuthApi.md#listorganizationaccess) | **GET** /v1/auth/organizations | List the caller\&#39;s active organization access |
| [**logout**](AuthApi.md#logout) | **POST** /v1/auth/logout | End session |
| [**refreshSession**](AuthApi.md#refreshsession) | **POST** /v1/auth/refresh | Refresh session |
| [**switchOrganization**](AuthApi.md#switchorganizationoperation) | **POST** /v1/auth/organization | Select an organization and issue a session with its current capabilities |



## createSession

> CreateSessionResponse createSession(createSessionRequest)

Start session

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { CreateSessionOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new AuthApi();

  const body = {
    // CreateSessionRequest
    createSessionRequest: ...,
  } satisfies CreateSessionOperationRequest;

  try {
    const data = await api.createSession(body);
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
| **createSessionRequest** | [CreateSessionRequest](CreateSessionRequest.md) |  | |

### Return type

[**CreateSessionResponse**](CreateSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getMe

> CallerContext getMe()

Current caller context

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { GetMeRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AuthApi(config);

  try {
    const data = await api.getMe();
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

[**CallerContext**](CallerContext.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Caller context |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listOrganizationAccess

> Array&lt;OrganizationAccess&gt; listOrganizationAccess()

List the caller\&#39;s active organization access

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { ListOrganizationAccessRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AuthApi(config);

  try {
    const data = await api.listOrganizationAccess();
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

[**Array&lt;OrganizationAccess&gt;**](OrganizationAccess.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Organizations with effective personas |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## logout

> SimpleOKResponse logout()

End session

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { LogoutRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new AuthApi();

  try {
    const data = await api.logout();
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

[**SimpleOKResponse**](SimpleOKResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session cleared |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## refreshSession

> CreateSessionResponse refreshSession()

Refresh session

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { RefreshSessionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new AuthApi();

  try {
    const data = await api.refreshSession();
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

[**CreateSessionResponse**](CreateSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session refreshed |  -  |
| **401** | Missing or invalid authentication |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## switchOrganization

> CreateSessionResponse switchOrganization(switchOrganizationRequest)

Select an organization and issue a session with its current capabilities

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '';
import type { SwitchOrganizationOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AuthApi(config);

  const body = {
    // SwitchOrganizationRequest
    switchOrganizationRequest: ...,
  } satisfies SwitchOrganizationOperationRequest;

  try {
    const data = await api.switchOrganization(body);
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
| **switchOrganizationRequest** | [SwitchOrganizationRequest](SwitchOrganizationRequest.md) |  | |

### Return type

[**CreateSessionResponse**](CreateSessionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Organization selected and session cookies rotated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

