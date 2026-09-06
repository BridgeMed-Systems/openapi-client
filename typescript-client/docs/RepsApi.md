# RepsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createRepAvailabilityWindow**](RepsApi.md#createrepavailabilitywindow) | **POST** /v1/reps/{repUserID}/availability/windows | Create representative availability window |
| [**deleteRepAvailabilityWindow**](RepsApi.md#deleterepavailabilitywindow) | **DELETE** /v1/reps/{repUserID}/availability/windows/{windowID} | Delete representative availability window |
| [**getRepAvailability**](RepsApi.md#getrepavailability) | **GET** /v1/reps/{repUserID}/availability | Get representative availability profile |
| [**listRepAccounts**](RepsApi.md#listrepaccounts) | **GET** /v1/reps/accounts | List accounts supported by assigned rep products |
| [**listRepAvailabilityWindows**](RepsApi.md#listrepavailabilitywindows) | **GET** /v1/reps/{repUserID}/availability/windows | List representative availability windows |
| [**listRepTeam**](RepsApi.md#listrepteam) | **GET** /v1/reps/team | View the current vendor team and coverage choices |
| [**listReps**](RepsApi.md#listreps) | **GET** /v1/reps/ | List representative directory entries |
| [**putRepAvailability**](RepsApi.md#putrepavailability) | **PUT** /v1/reps/{repUserID}/availability | Upsert representative availability profile |
| [**updateRepAvailabilityWindow**](RepsApi.md#updaterepavailabilitywindow) | **PATCH** /v1/reps/{repUserID}/availability/windows/{windowID} | Update representative availability window |
| [**updateRepTeamMember**](RepsApi.md#updaterepteammember) | **PUT** /v1/reps/team/{repUserID} | Update an existing representative\&#39;s company contact and mappings |



## createRepAvailabilityWindow

> RepAvailabilityWindow createRepAvailabilityWindow(repUserID, upsertRepAvailabilityWindowRequest)

Create representative availability window

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { CreateRepAvailabilityWindowRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpsertRepAvailabilityWindowRequest
    upsertRepAvailabilityWindowRequest: ...,
  } satisfies CreateRepAvailabilityWindowRequest;

  try {
    const data = await api.createRepAvailabilityWindow(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |
| **upsertRepAvailabilityWindowRequest** | [UpsertRepAvailabilityWindowRequest](UpsertRepAvailabilityWindowRequest.md) |  | |

### Return type

[**RepAvailabilityWindow**](RepAvailabilityWindow.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Representative availability window created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteRepAvailabilityWindow

> deleteRepAvailabilityWindow(repUserID, windowID)

Delete representative availability window

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { DeleteRepAvailabilityWindowRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    windowID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeleteRepAvailabilityWindowRequest;

  try {
    const data = await api.deleteRepAvailabilityWindow(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |
| **windowID** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Representative availability window removed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getRepAvailability

> RepAvailabilityProfile getRepAvailability(repUserID)

Get representative availability profile

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { GetRepAvailabilityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetRepAvailabilityRequest;

  try {
    const data = await api.getRepAvailability(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |

### Return type

[**RepAvailabilityProfile**](RepAvailabilityProfile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Representative availability profile |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listRepAccounts

> Array&lt;RepAssignedAccount&gt; listRepAccounts(scope)

List accounts supported by assigned rep products

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { ListRepAccountsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // 'assigned'
    scope: scope_example,
  } satisfies ListRepAccountsRequest;

  try {
    const data = await api.listRepAccounts(body);
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
| **scope** | `assigned` |  | [Defaults to `undefined`] [Enum: assigned] |

### Return type

[**Array&lt;RepAssignedAccount&gt;**](RepAssignedAccount.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rep-supported accounts |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listRepAvailabilityWindows

> Array&lt;RepAvailabilityWindow&gt; listRepAvailabilityWindows(repUserID)

List representative availability windows

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { ListRepAvailabilityWindowsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListRepAvailabilityWindowsRequest;

  try {
    const data = await api.listRepAvailabilityWindows(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Array&lt;RepAvailabilityWindow&gt;**](RepAvailabilityWindow.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Representative availability windows |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listRepTeam

> RepTeam listRepTeam()

View the current vendor team and coverage choices

Vendor admins see existing company reps; regional managers see themselves and their assigned team. Contains no learning or compliance records.

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { ListRepTeamRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  try {
    const data = await api.listRepTeam();
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

[**RepTeam**](RepTeam.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Team and permitted product/account choices |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listReps

> Array&lt;RepDirectoryEntry&gt; listReps()

List representative directory entries

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { ListRepsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  try {
    const data = await api.listReps();
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

[**Array&lt;RepDirectoryEntry&gt;**](RepDirectoryEntry.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Representative directory entries |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## putRepAvailability

> RepAvailabilityProfile putRepAvailability(repUserID, upsertRepAvailabilityProfileRequest)

Upsert representative availability profile

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { PutRepAvailabilityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpsertRepAvailabilityProfileRequest
    upsertRepAvailabilityProfileRequest: ...,
  } satisfies PutRepAvailabilityRequest;

  try {
    const data = await api.putRepAvailability(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |
| **upsertRepAvailabilityProfileRequest** | [UpsertRepAvailabilityProfileRequest](UpsertRepAvailabilityProfileRequest.md) |  | |

### Return type

[**RepAvailabilityProfile**](RepAvailabilityProfile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Representative availability profile |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateRepAvailabilityWindow

> RepAvailabilityWindow updateRepAvailabilityWindow(repUserID, windowID, upsertRepAvailabilityWindowRequest)

Update representative availability window

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { UpdateRepAvailabilityWindowRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    windowID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpsertRepAvailabilityWindowRequest
    upsertRepAvailabilityWindowRequest: ...,
  } satisfies UpdateRepAvailabilityWindowRequest;

  try {
    const data = await api.updateRepAvailabilityWindow(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |
| **windowID** | `string` |  | [Defaults to `undefined`] |
| **upsertRepAvailabilityWindowRequest** | [UpsertRepAvailabilityWindowRequest](UpsertRepAvailabilityWindowRequest.md) |  | |

### Return type

[**RepAvailabilityWindow**](RepAvailabilityWindow.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Representative availability window |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateRepTeamMember

> updateRepTeamMember(repUserID, repTeamUpdate)

Update an existing representative\&#39;s company contact and mappings

Vendor organization admins only. Replaces this company\&#39;s contact, product/account mappings, manager assignment and permitted rep role atomically. Does not change login identity or create/remove accounts. Revision mismatches return 409. Role changes invalidate prior sessions.

### Example

```ts
import {
  Configuration,
  RepsApi,
} from '';
import type { UpdateRepTeamMemberRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RepsApi(config);

  const body = {
    // string
    repUserID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RepTeamUpdate
    repTeamUpdate: ...,
  } satisfies UpdateRepTeamMemberRequest;

  try {
    const data = await api.updateRepTeamMember(body);
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
| **repUserID** | `string` |  | [Defaults to `undefined`] |
| **repTeamUpdate** | [RepTeamUpdate](RepTeamUpdate.md) |  | |

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
| **204** | Representative updated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

