# AdminApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAdminUser**](AdminApi.md#createadminuseroperation) | **POST** /v1/admin/users | Create admin user |
| [**getAdminUserAuthorization**](AdminApi.md#getadminuserauthorization) | **GET** /v1/admin/users/{id}/authorization | Get user authorization state |
| [**listAdminAuditEvents**](AdminApi.md#listadminauditevents) | **GET** /v1/admin/audit/events | List audit events (admin cursor view) |
| [**listAdminOrganizations**](AdminApi.md#listadminorganizations) | **GET** /v1/admin/organizations | List organizations (admin cursor view) |
| [**listAdminProducts**](AdminApi.md#listadminproducts) | **GET** /v1/admin/products | List products (admin cursor view) |
| [**listAdminTrainingRequests**](AdminApi.md#listadmintrainingrequests) | **GET** /v1/admin/training/requests | List training requests (admin cursor view) |
| [**listAdminUsers**](AdminApi.md#listadminusers) | **GET** /v1/admin/users | List users (admin cursor view) |
| [**listAdminWebinars**](AdminApi.md#listadminwebinars) | **GET** /v1/admin/webinars | List webinars (admin cursor view) |
| [**updateAdminUserAuthorization**](AdminApi.md#updateadminuserauthorizationoperation) | **PUT** /v1/admin/users/{id}/authorization | Replace user persona and permission overrides |



## createAdminUser

> User createAdminUser(createAdminUserRequest)

Create admin user

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { CreateAdminUserOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // CreateAdminUserRequest
    createAdminUserRequest: ...,
  } satisfies CreateAdminUserOperationRequest;

  try {
    const data = await api.createAdminUser(body);
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
| **createAdminUserRequest** | [CreateAdminUserRequest](CreateAdminUserRequest.md) |  | |

### Return type

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Admin user created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getAdminUserAuthorization

> AdminUserAuthorization getAdminUserAuthorization(userID)

Get user authorization state

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { GetAdminUserAuthorizationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetAdminUserAuthorizationRequest;

  try {
    const data = await api.getAdminUserAuthorization(body);
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
| **userID** | `string` |  | [Defaults to `undefined`] |

### Return type

[**AdminUserAuthorization**](AdminUserAuthorization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User authorization state |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminAuditEvents

> CursorPageAuditEvent listAdminAuditEvents(actorUserId, action, entityType, entityId, organizationId, from, to, limit, cursor)

List audit events (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminAuditEventsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    actorUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    action: action_example,
    // string (optional)
    entityType: entityType_example,
    // string (optional)
    entityId: entityId_example,
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // Date (optional)
    from: 2013-10-20T19:20:30+01:00,
    // Date (optional)
    to: 2013-10-20T19:20:30+01:00,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminAuditEventsRequest;

  try {
    const data = await api.listAdminAuditEvents(body);
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
| **actorUserId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **action** | `string` |  | [Optional] [Defaults to `undefined`] |
| **entityType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **entityId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **organizationId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **from** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **to** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageAuditEvent**](CursorPageAuditEvent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of audit events |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminOrganizations

> CursorPageOrganization listAdminOrganizations(q, orgType, onboardingStatus, limit, cursor)

List organizations (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminOrganizationsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // OrganizationType (optional)
    orgType: ...,
    // OnboardingState (optional)
    onboardingStatus: ...,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminOrganizationsRequest;

  try {
    const data = await api.listAdminOrganizations(body);
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
| **orgType** | `OrganizationType` |  | [Optional] [Defaults to `undefined`] [Enum: hospital, vendor, health_system, other] |
| **onboardingStatus** | `OnboardingState` |  | [Optional] [Defaults to `undefined`] [Enum: prospect, invited, in_progress, active, inactive] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageOrganization**](CursorPageOrganization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of organizations |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminProducts

> CursorPageProduct listAdminProducts(q, vendorOrgId, limit, cursor)

List products (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminProductsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    vendorOrgId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminProductsRequest;

  try {
    const data = await api.listAdminProducts(body);
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
| **vendorOrgId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageProduct**](CursorPageProduct.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of products |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminTrainingRequests

> CursorPageTrainingRequest listAdminTrainingRequests(organizationId, submittedByUserId, assignedUserId, statuses, limit, cursor)

List training requests (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminTrainingRequestsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    submittedByUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    assignedUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    statuses: statuses_example,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminTrainingRequestsRequest;

  try {
    const data = await api.listAdminTrainingRequests(body);
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
| **statuses** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageTrainingRequest**](CursorPageTrainingRequest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of training requests |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminUsers

> CursorPageUser listAdminUsers(q, persona, status, organizationId, limit, cursor)

List users (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminUsersRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // UserPersona (optional)
    persona: ...,
    // UserStatus (optional)
    status: ...,
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminUsersRequest;

  try {
    const data = await api.listAdminUsers(body);
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
| **persona** | `UserPersona` |  | [Optional] [Defaults to `undefined`] [Enum: user, representative, admin] |
| **status** | `UserStatus` |  | [Optional] [Defaults to `undefined`] [Enum: active, inactive, pending] |
| **organizationId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageUser**](CursorPageUser.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of users |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listAdminWebinars

> CursorPageWebinar listAdminWebinars(organizationId, hostUserId, statuses, start, end, limit, cursor)

List webinars (admin cursor view)

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { ListAdminWebinarsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    hostUserId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    statuses: statuses_example,
    // Date (optional)
    start: 2013-10-20T19:20:30+01:00,
    // Date (optional)
    end: 2013-10-20T19:20:30+01:00,
    // number (optional)
    limit: 56,
    // string (optional)
    cursor: cursor_example,
  } satisfies ListAdminWebinarsRequest;

  try {
    const data = await api.listAdminWebinars(body);
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
| **statuses** | `string` |  | [Optional] [Defaults to `undefined`] |
| **start** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **end** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `25`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CursorPageWebinar**](CursorPageWebinar.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Cursor page of webinars |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateAdminUserAuthorization

> AdminUserAuthorization updateAdminUserAuthorization(userID, updateAdminUserAuthorizationRequest)

Replace user persona and permission overrides

### Example

```ts
import {
  Configuration,
  AdminApi,
} from '';
import type { UpdateAdminUserAuthorizationOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AdminApi(config);

  const body = {
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateAdminUserAuthorizationRequest
    updateAdminUserAuthorizationRequest: ...,
  } satisfies UpdateAdminUserAuthorizationOperationRequest;

  try {
    const data = await api.updateAdminUserAuthorization(body);
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
| **userID** | `string` |  | [Defaults to `undefined`] |
| **updateAdminUserAuthorizationRequest** | [UpdateAdminUserAuthorizationRequest](UpdateAdminUserAuthorizationRequest.md) |  | |

### Return type

[**AdminUserAuthorization**](AdminUserAuthorization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated user authorization state |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

