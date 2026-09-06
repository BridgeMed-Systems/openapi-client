# UsersApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**acceptUserInvite**](UsersApi.md#acceptuserinvite) | **POST** /v1/users/invites/accept | Accept invite and create credentials |
| [**completeVendorSignup**](UsersApi.md#completevendorsignup) | **POST** /v1/vendor-signups/complete | Create a new vendor organization after email verification |
| [**createHospitalDepartment**](UsersApi.md#createhospitaldepartmentoperation) | **POST** /v1/staff/departments | Add a hospital department |
| [**createUserInvite**](UsersApi.md#createuserinvite) | **POST** /v1/users/invites | Create and email an organization invitation |
| [**getUserById**](UsersApi.md#getuserbyid) | **GET** /v1/users/{id} | Get user by id |
| [**listHospitalDepartments**](UsersApi.md#listhospitaldepartments) | **GET** /v1/staff/departments | List departments in the current hospital |
| [**listHospitalStaff**](UsersApi.md#listhospitalstaff) | **GET** /v1/staff/ | List staff in the current hospital |
| [**previewVendorSignup**](UsersApi.md#previewvendorsignup) | **POST** /v1/vendor-signups/preview | Review an email-verified signup link |
| [**removeHospitalDepartment**](UsersApi.md#removehospitaldepartment) | **DELETE** /v1/staff/departments/{id} | Remove an empty hospital department |
| [**removeHospitalStaff**](UsersApi.md#removehospitalstaff) | **DELETE** /v1/staff/{id} | Remove hospital membership while retaining the global account and history |
| [**requestPasswordRecovery**](UsersApi.md#requestpasswordrecovery) | **POST** /v1/users/password/recovery | Email a one-use password recovery link |
| [**requestVendorSignup**](UsersApi.md#requestvendorsignup) | **POST** /v1/vendor-signups | Request email verification for a new vendor organization |
| [**resetPassword**](UsersApi.md#resetpassword) | **POST** /v1/users/password/reset | Reset a password and invalidate previous sessions |
| [**updateHospitalDepartment**](UsersApi.md#updatehospitaldepartment) | **PUT** /v1/staff/departments/{id} | Rename a hospital department |
| [**updateHospitalStaff**](UsersApi.md#updatehospitalstaff) | **PUT** /v1/staff/{id} | Change a hospital staff member\&#39;s role and department |



## acceptUserInvite

> User acceptUserInvite(acceptInviteRequest)

Accept invite and create credentials

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { AcceptUserInviteRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // AcceptInviteRequest
    acceptInviteRequest: ...,
  } satisfies AcceptUserInviteRequest;

  try {
    const data = await api.acceptUserInvite(body);
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
| **acceptInviteRequest** | [AcceptInviteRequest](AcceptInviteRequest.md) |  | |

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | User accepted invite |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## completeVendorSignup

> VendorSignupResult completeVendorSignup(vendorSignupComplete)

Create a new vendor organization after email verification

Public, rate-limited JSON endpoint. Tokens are carried only in request bodies, never URLs. Verification links expire after 24 hours and grant no access to existing organizations. Responses use private, no-store caching.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { CompleteVendorSignupRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // VendorSignupComplete
    vendorSignupComplete: ...,
  } satisfies CompleteVendorSignupRequest;

  try {
    const data = await api.completeVendorSignup(body);
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
| **vendorSignupComplete** | [VendorSignupComplete](VendorSignupComplete.md) |  | |

### Return type

[**VendorSignupResult**](VendorSignupResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Signup result |  -  |
| **400** | Invalid input, missing owner attestation or unsupported password |  -  |
| **401** | Invalid, expired or used link; existing account requires its current password |  -  |
| **409** | Company name reserved or concurrent account creation; no existing organization access granted |  -  |
| **415** | application/json is required |  -  |
| **429** | Request limit reached; Retry-After indicates the maximum remaining window |  -  |
| **503** | Signup, delivery queue or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createHospitalDepartment

> HospitalDepartment createHospitalDepartment(createHospitalDepartmentRequest)

Add a hospital department

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { CreateHospitalDepartmentOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // CreateHospitalDepartmentRequest
    createHospitalDepartmentRequest: ...,
  } satisfies CreateHospitalDepartmentOperationRequest;

  try {
    const data = await api.createHospitalDepartment(body);
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
| **createHospitalDepartmentRequest** | [CreateHospitalDepartmentRequest](CreateHospitalDepartmentRequest.md) |  | |

### Return type

[**HospitalDepartment**](HospitalDepartment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Hospital department |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createUserInvite

> CreateInviteResponse createUserInvite(createInviteRequest)

Create and email an organization invitation

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { CreateUserInviteRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // CreateInviteRequest
    createInviteRequest: ...,
  } satisfies CreateUserInviteRequest;

  try {
    const data = await api.createUserInvite(body);
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
| **createInviteRequest** | [CreateInviteRequest](CreateInviteRequest.md) |  | |

### Return type

[**CreateInviteResponse**](CreateInviteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Invite created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getUserById

> User getUserById(id)

Get user by id

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { GetUserByIdRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetUserByIdRequest;

  try {
    const data = await api.getUserById(body);
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

[**User**](User.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listHospitalDepartments

> Array&lt;HospitalDepartment&gt; listHospitalDepartments()

List departments in the current hospital

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { ListHospitalDepartmentsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  try {
    const data = await api.listHospitalDepartments();
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

[**Array&lt;HospitalDepartment&gt;**](HospitalDepartment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Departments |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listHospitalStaff

> Array&lt;HospitalStaffMember&gt; listHospitalStaff()

List staff in the current hospital

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { ListHospitalStaffRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  try {
    const data = await api.listHospitalStaff();
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

[**Array&lt;HospitalStaffMember&gt;**](HospitalStaffMember.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hospital staff |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## previewVendorSignup

> VendorSignupPreview previewVendorSignup(vendorSignupToken)

Review an email-verified signup link

Public, rate-limited JSON endpoint. Tokens are carried only in request bodies, never URLs. Verification links expire after 24 hours and grant no access to existing organizations. Responses use private, no-store caching.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { PreviewVendorSignupRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // VendorSignupToken
    vendorSignupToken: ...,
  } satisfies PreviewVendorSignupRequest;

  try {
    const data = await api.previewVendorSignup(body);
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
| **vendorSignupToken** | [VendorSignupToken](VendorSignupToken.md) |  | |

### Return type

[**VendorSignupPreview**](VendorSignupPreview.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Signup result |  -  |
| **400** | Invalid verification request |  -  |
| **401** | Invalid, expired or used verification link |  -  |
| **415** | application/json is required |  -  |
| **429** | Request limit reached; Retry-After indicates the maximum remaining window |  -  |
| **503** | Signup, delivery queue or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## removeHospitalDepartment

> removeHospitalDepartment(id)

Remove an empty hospital department

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { RemoveHospitalDepartmentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies RemoveHospitalDepartmentRequest;

  try {
    const data = await api.removeHospitalDepartment(body);
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
| **204** | Department removed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## removeHospitalStaff

> removeHospitalStaff(id)

Remove hospital membership while retaining the global account and history

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { RemoveHospitalStaffRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies RemoveHospitalStaffRequest;

  try {
    const data = await api.removeHospitalStaff(body);
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
| **204** | Membership removed and prior sessions invalidated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## requestPasswordRecovery

> RequestPasswordRecovery202Response requestPasswordRecovery(passwordRecoveryRequest)

Email a one-use password recovery link

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { RequestPasswordRecoveryRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // PasswordRecoveryRequest
    passwordRecoveryRequest: ...,
  } satisfies RequestPasswordRecoveryRequest;

  try {
    const data = await api.requestPasswordRecovery(body);
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
| **passwordRecoveryRequest** | [PasswordRecoveryRequest](PasswordRecoveryRequest.md) |  | |

### Return type

[**RequestPasswordRecovery202Response**](RequestPasswordRecovery202Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Same response for known, unknown, and throttled addresses |  -  |
| **400** | Validation or request shape error |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## requestVendorSignup

> VendorSignupAccepted requestVendorSignup(vendorSignupInput)

Request email verification for a new vendor organization

Public, rate-limited JSON endpoint. Tokens are carried only in request bodies, never URLs. Verification links expire after 24 hours and grant no access to existing organizations. Responses use private, no-store caching.

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { RequestVendorSignupRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // VendorSignupInput
    vendorSignupInput: ...,
  } satisfies RequestVendorSignupRequest;

  try {
    const data = await api.requestVendorSignup(body);
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
| **vendorSignupInput** | [VendorSignupInput](VendorSignupInput.md) |  | |

### Return type

[**VendorSignupAccepted**](VendorSignupAccepted.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Verification email durably queued; no account or subscription created |  -  |
| **400** | Invalid company or contact input |  -  |
| **415** | application/json is required |  -  |
| **429** | Request limit reached; Retry-After indicates the maximum remaining window |  -  |
| **503** | Signup, delivery queue or request limiter temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## resetPassword

> resetPassword(passwordResetRequest)

Reset a password and invalidate previous sessions

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { ResetPasswordRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new UsersApi();

  const body = {
    // PasswordResetRequest
    passwordResetRequest: ...,
  } satisfies ResetPasswordRequest;

  try {
    const data = await api.resetPassword(body);
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
| **passwordResetRequest** | [PasswordResetRequest](PasswordResetRequest.md) |  | |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Password changed; sign in again |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **429** | Too many attempts |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateHospitalDepartment

> HospitalDepartment updateHospitalDepartment(id, createHospitalDepartmentRequest)

Rename a hospital department

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { UpdateHospitalDepartmentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateHospitalDepartmentRequest
    createHospitalDepartmentRequest: ...,
  } satisfies UpdateHospitalDepartmentRequest;

  try {
    const data = await api.updateHospitalDepartment(body);
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
| **createHospitalDepartmentRequest** | [CreateHospitalDepartmentRequest](CreateHospitalDepartmentRequest.md) |  | |

### Return type

[**HospitalDepartment**](HospitalDepartment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Hospital department |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateHospitalStaff

> updateHospitalStaff(id, hospitalStaffUpdate)

Change a hospital staff member\&#39;s role and department

### Example

```ts
import {
  Configuration,
  UsersApi,
} from '';
import type { UpdateHospitalStaffRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UsersApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // HospitalStaffUpdate
    hospitalStaffUpdate: ...,
  } satisfies UpdateHospitalStaffRequest;

  try {
    const data = await api.updateHospitalStaff(body);
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
| **hospitalStaffUpdate** | [HospitalStaffUpdate](HospitalStaffUpdate.md) |  | |

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
| **204** | Access updated and prior sessions invalidated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

