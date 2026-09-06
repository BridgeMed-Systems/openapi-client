# EducationApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addEducationVersion**](EducationApi.md#addeducationversion) | **POST** /v1/education/courses/{id}/versions | Save a new immutable course version |
| [**createEducationCourse**](EducationApi.md#createeducationcourse) | **POST** /v1/education/courses | Save a vendor course and its first immutable draft |
| [**getEducationCourse**](EducationApi.md#geteducationcourse) | **GET** /v1/education/courses/{id} | Read course details and recent version metadata |
| [**getEducationVersion**](EducationApi.md#geteducationversion) | **GET** /v1/education/versions/{id} | Read authorized lessons and quiz choices |
| [**listEducationCourses**](EducationApi.md#listeducationcourses) | **GET** /v1/education/courses | Find visible education courses |
| [**publishEducationVersion**](EducationApi.md#publisheducationversion) | **POST** /v1/education/versions/{id}/publish | Publish a validated course version |
| [**withdrawEducationVersion**](EducationApi.md#withdraweducationversion) | **POST** /v1/education/versions/{id}/withdraw | Withdraw a course version permanently |



## addEducationVersion

> EducationVersion addEducationVersion(id, idempotencyKey, educationVersionDraft)

Save a new immutable course version

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { AddEducationVersionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string | Retry the exact submission with the same UUID. Changed details require a new key.
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // EducationVersionDraft
    educationVersionDraft: ...,
  } satisfies AddEducationVersionRequest;

  try {
    const data = await api.addEducationVersion(body);
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
| **idempotencyKey** | `string` | Retry the exact submission with the same UUID. Changed details require a new key. | [Defaults to `undefined`] |
| **educationVersionDraft** | [EducationVersionDraft](EducationVersionDraft.md) |  | |

### Return type

[**EducationVersion**](EducationVersion.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createEducationCourse

> EducationCourse createEducationCourse(idempotencyKey, createEducationCourse)

Save a vendor course and its first immutable draft

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { CreateEducationCourseRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string | Retry the exact submission with the same UUID. Changed details require a new key.
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateEducationCourse
    createEducationCourse: ...,
  } satisfies CreateEducationCourseRequest;

  try {
    const data = await api.createEducationCourse(body);
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
| **idempotencyKey** | `string` | Retry the exact submission with the same UUID. Changed details require a new key. | [Defaults to `undefined`] |
| **createEducationCourse** | [CreateEducationCourse](CreateEducationCourse.md) |  | |

### Return type

[**EducationCourse**](EducationCourse.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getEducationCourse

> EducationCourse getEducationCourse(id)

Read course details and recent version metadata

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { GetEducationCourseRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetEducationCourseRequest;

  try {
    const data = await api.getEducationCourse(body);
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

[**EducationCourse**](EducationCourse.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getEducationVersion

> EducationVersion getEducationVersion(id)

Read authorized lessons and quiz choices

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { GetEducationVersionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetEducationVersionRequest;

  try {
    const data = await api.getEducationVersion(body);
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

[**EducationVersion**](EducationVersion.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listEducationCourses

> EducationCoursePage listEducationCourses(q, limit, offset)

Find visible education courses

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { ListEducationCoursesRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListEducationCoursesRequest;

  try {
    const data = await api.listEducationCourses(body);
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

[**EducationCoursePage**](EducationCoursePage.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publishEducationVersion

> EducationVersion publishEducationVersion(id)

Publish a validated course version

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { PublishEducationVersionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies PublishEducationVersionRequest;

  try {
    const data = await api.publishEducationVersion(body);
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

[**EducationVersion**](EducationVersion.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## withdrawEducationVersion

> EducationVersion withdrawEducationVersion(id, educationWithdrawal)

Withdraw a course version permanently

Requires education.withdraw for the current vendor administrator. Independent of publication access; existing explicit education.author denies still block withdrawal. Material and credit metadata cannot change through this action.

### Example

```ts
import {
  Configuration,
  EducationApi,
} from '';
import type { WithdrawEducationVersionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EducationApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // EducationWithdrawal
    educationWithdrawal: ...,
  } satisfies WithdrawEducationVersionRequest;

  try {
    const data = await api.withdrawEducationVersion(body);
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
| **educationWithdrawal** | [EducationWithdrawal](EducationWithdrawal.md) |  | |

### Return type

[**EducationVersion**](EducationVersion.md)

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
| **403** | Operation is not permitted |  -  |
| **404** | Course or version is unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

