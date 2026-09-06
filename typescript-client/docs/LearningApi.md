# LearningApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**acknowledgeLearningLesson**](LearningApi.md#acknowledgelearninglesson) | **PUT** /v1/learning/attempts/{id}/lessons/{lesson} | Acknowledge a lesson and the displayed document revision |
| [**createLearningRequirement**](LearningApi.md#createlearningrequirement) | **POST** /v1/learning/requirements | Assign a published course version to current and future scope members |
| [**enrollInEducation**](LearningApi.md#enrollineducation) | **POST** /v1/learning/enroll | Add a visible course to personal learning |
| [**exportHospitalLearningCompliance**](LearningApi.md#exporthospitallearningcompliance) | **GET** /v1/learning/compliance.csv | Export filtered hospital compliance from one consistent record set |
| [**getLearningCompletion**](LearningApi.md#getlearningcompletion) | **GET** /v1/learning/completions/{id} | Read a certificate record as its learner or owning hospital administrator |
| [**getLearningDetail**](LearningApi.md#getlearningdetail) | **GET** /v1/learning/enrollments/{id} | Read authorized learning progress and course materials |
| [**listHospitalLearningCompliance**](LearningApi.md#listhospitallearningcompliance) | **GET** /v1/learning/compliance | Report current hospital learner compliance |
| [**listLearningHistory**](LearningApi.md#listlearninghistory) | **GET** /v1/learning/history | Read immutable personal completion history across hospital memberships |
| [**listLearningRequirements**](LearningApi.md#listlearningrequirements) | **GET** /v1/learning/requirements | List ongoing hospital requirements |
| [**listMyLearning**](LearningApi.md#listmylearning) | **GET** /v1/learning/my | List personal current learning |
| [**setLearningRequirementEnabled**](LearningApi.md#setlearningrequirementenabled) | **PUT** /v1/learning/requirements/{id} | Enable or stop an ongoing hospital requirement |
| [**startLearningAttempt**](LearningApi.md#startlearningattempt) | **POST** /v1/learning/enrollments/{id}/start | Start or resume personal learning without duplicating a valid completion |
| [**submitLearningAttempt**](LearningApi.md#submitlearningattempt) | **POST** /v1/learning/attempts/{id}/submit | Grade configured criteria and atomically issue completion and provider credit |



## acknowledgeLearningLesson

> LearningDetail acknowledgeLearningLesson(id, lesson, learningAcknowledgement)

Acknowledge a lesson and the displayed document revision

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { AcknowledgeLearningLessonRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    lesson: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // LearningAcknowledgement
    learningAcknowledgement: ...,
  } satisfies AcknowledgeLearningLessonRequest;

  try {
    const data = await api.acknowledgeLearningLesson(body);
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
| **lesson** | `string` |  | [Defaults to `undefined`] |
| **learningAcknowledgement** | [LearningAcknowledgement](LearningAcknowledgement.md) |  | |

### Return type

[**LearningDetail**](LearningDetail.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createLearningRequirement

> LearningRequirement createLearningRequirement(idempotencyKey, learningRequirementInput)

Assign a published course version to current and future scope members

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { CreateLearningRequirementRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // LearningRequirementInput
    learningRequirementInput: ...,
  } satisfies CreateLearningRequirementRequest;

  try {
    const data = await api.createLearningRequirement(body);
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
| **idempotencyKey** | `string` |  | [Defaults to `undefined`] |
| **learningRequirementInput** | [LearningRequirementInput](LearningRequirementInput.md) |  | |

### Return type

[**LearningRequirement**](LearningRequirement.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## enrollInEducation

> LearningDetail enrollInEducation(learningEnrollmentRequest)

Add a visible course to personal learning

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { EnrollInEducationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // LearningEnrollmentRequest
    learningEnrollmentRequest: ...,
  } satisfies EnrollInEducationRequest;

  try {
    const data = await api.enrollInEducation(body);
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
| **learningEnrollmentRequest** | [LearningEnrollmentRequest](LearningEnrollmentRequest.md) |  | |

### Return type

[**LearningDetail**](LearningDetail.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## exportHospitalLearningCompliance

> Blob exportHospitalLearningCompliance(q, state, departmentId)

Export filtered hospital compliance from one consistent record set

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { ExportHospitalLearningComplianceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    state: state_example,
    // string (optional)
    departmentId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ExportHospitalLearningComplianceRequest;

  try {
    const data = await api.exportHospitalLearningCompliance(body);
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
| **state** | `string` |  | [Optional] [Defaults to `undefined`] |
| **departmentId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

**Blob**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/csv`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |
| **400** | Invalid submission |  -  |
| **401** | Sign in required |  -  |
| **403** | Operation is not permitted |  -  |
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getLearningCompletion

> LearningCompletion getLearningCompletion(id)

Read a certificate record as its learner or owning hospital administrator

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { GetLearningCompletionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetLearningCompletionRequest;

  try {
    const data = await api.getLearningCompletion(body);
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

[**LearningCompletion**](LearningCompletion.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getLearningDetail

> LearningDetail getLearningDetail(id)

Read authorized learning progress and course materials

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { GetLearningDetailRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetLearningDetailRequest;

  try {
    const data = await api.getLearningDetail(body);
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

[**LearningDetail**](LearningDetail.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listHospitalLearningCompliance

> LearningEnrollmentPage listHospitalLearningCompliance(q, state, departmentId, limit, offset)

Report current hospital learner compliance

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { ListHospitalLearningComplianceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    state: state_example,
    // string (optional)
    departmentId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListHospitalLearningComplianceRequest;

  try {
    const data = await api.listHospitalLearningCompliance(body);
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
| **state** | `string` |  | [Optional] [Defaults to `undefined`] |
| **departmentId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**LearningEnrollmentPage**](LearningEnrollmentPage.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listLearningHistory

> LearningCompletionPage listLearningHistory(q, limit, offset)

Read immutable personal completion history across hospital memberships

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { ListLearningHistoryRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListLearningHistoryRequest;

  try {
    const data = await api.listLearningHistory(body);
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

[**LearningCompletionPage**](LearningCompletionPage.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listLearningRequirements

> LearningRequirementPage listLearningRequirements(q, state, departmentId, limit, offset)

List ongoing hospital requirements

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { ListLearningRequirementsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    state: state_example,
    // string (optional)
    departmentId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListLearningRequirementsRequest;

  try {
    const data = await api.listLearningRequirements(body);
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
| **state** | `string` |  | [Optional] [Defaults to `undefined`] |
| **departmentId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**LearningRequirementPage**](LearningRequirementPage.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listMyLearning

> LearningEnrollmentPage listMyLearning(q, state, departmentId, limit, offset)

List personal current learning

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { ListMyLearningRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    state: state_example,
    // string (optional)
    departmentId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListMyLearningRequest;

  try {
    const data = await api.listMyLearning(body);
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
| **state** | `string` |  | [Optional] [Defaults to `undefined`] |
| **departmentId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**LearningEnrollmentPage**](LearningEnrollmentPage.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## setLearningRequirementEnabled

> LearningRequirement setLearningRequirementEnabled(id, learningRequirementStatus)

Enable or stop an ongoing hospital requirement

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { SetLearningRequirementEnabledRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // LearningRequirementStatus
    learningRequirementStatus: ...,
  } satisfies SetLearningRequirementEnabledRequest;

  try {
    const data = await api.setLearningRequirementEnabled(body);
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
| **learningRequirementStatus** | [LearningRequirementStatus](LearningRequirementStatus.md) |  | |

### Return type

[**LearningRequirement**](LearningRequirement.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startLearningAttempt

> LearningDetail startLearningAttempt(id)

Start or resume personal learning without duplicating a valid completion

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { StartLearningAttemptRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies StartLearningAttemptRequest;

  try {
    const data = await api.startLearningAttempt(body);
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

[**LearningDetail**](LearningDetail.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## submitLearningAttempt

> LearningSubmission submitLearningAttempt(id, idempotencyKey, learningSubmissionRequest)

Grade configured criteria and atomically issue completion and provider credit

### Example

```ts
import {
  Configuration,
  LearningApi,
} from '';
import type { SubmitLearningAttemptRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LearningApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // LearningSubmissionRequest
    learningSubmissionRequest: ...,
  } satisfies SubmitLearningAttemptRequest;

  try {
    const data = await api.submitLearningAttempt(body);
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
| **idempotencyKey** | `string` |  | [Defaults to `undefined`] |
| **learningSubmissionRequest** | [LearningSubmissionRequest](LearningSubmissionRequest.md) |  | |

### Return type

[**LearningSubmission**](LearningSubmission.md)

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
| **404** | Record unavailable |  -  |
| **409** | Conflicting submission |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

