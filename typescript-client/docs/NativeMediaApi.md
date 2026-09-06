# NativeMediaApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**assignNativePresenter**](NativeMediaApi.md#assignnativepresenter) | **PUT** /v1/media/rooms/{id}/presenters/{userID} | Assign a presenter before the event starts |
| [**listNativeParticipants**](NativeMediaApi.md#listnativeparticipants) | **GET** /v1/media/rooms/{id}/participants | List current room participants and published tracks |
| [**listNativePresenters**](NativeMediaApi.md#listnativepresenters) | **GET** /v1/media/rooms/{id}/presenters | List the host and assigned presenters |
| [**moderateNativeParticipant**](NativeMediaApi.md#moderatenativeparticipant) | **POST** /v1/media/rooms/{id}/participants/{admissionID}/moderate | Mute a track or remove a participant |
| [**removeNativePresenter**](NativeMediaApi.md#removenativepresenter) | **DELETE** /v1/media/rooms/{id}/presenters/{userID} | Remove a presenter assignment before the event starts |



## assignNativePresenter

> assignNativePresenter(id, userID, nativePresenterInput)

Assign a presenter before the event starts

Host plus three additional presenters. Current event access is required. Repeating the same assignment is idempotent.

### Example

```ts
import {
  Configuration,
  NativeMediaApi,
} from '';
import type { AssignNativePresenterRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NativeMediaApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // NativePresenterInput
    nativePresenterInput: ...,
  } satisfies AssignNativePresenterRequest;

  try {
    const data = await api.assignNativePresenter(body);
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
| **userID** | `string` |  | [Defaults to `undefined`] |
| **nativePresenterInput** | [NativePresenterInput](NativePresenterInput.md) |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Presenter assigned |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listNativeParticipants

> Array&lt;NativeParticipant&gt; listNativeParticipants(id)

List current room participants and published tracks

Operational room state only, separate from durable learner records.

### Example

```ts
import {
  Configuration,
  NativeMediaApi,
} from '';
import type { ListNativeParticipantsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NativeMediaApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListNativeParticipantsRequest;

  try {
    const data = await api.listNativeParticipants(body);
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

[**Array&lt;NativeParticipant&gt;**](NativeParticipant.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current room state |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listNativePresenters

> Array&lt;NativePresenter&gt; listNativePresenters(id)

List the host and assigned presenters

### Example

```ts
import {
  Configuration,
  NativeMediaApi,
} from '';
import type { ListNativePresentersRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NativeMediaApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListNativePresentersRequest;

  try {
    const data = await api.listNativePresenters(body);
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

[**Array&lt;NativePresenter&gt;**](NativePresenter.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Current room state |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## moderateNativeParticipant

> moderateNativeParticipant(id, admissionID, nativeModerationInput)

Mute a track or remove a participant

Removal immediately denies future joins and reconnects, with retryable SFU removal. The host cannot be removed. Remote unmute is never allowed.

### Example

```ts
import {
  Configuration,
  NativeMediaApi,
} from '';
import type { ModerateNativeParticipantRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NativeMediaApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    admissionID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // NativeModerationInput
    nativeModerationInput: ...,
  } satisfies ModerateNativeParticipantRequest;

  try {
    const data = await api.moderateNativeParticipant(body);
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
| **admissionID** | `string` |  | [Defaults to `undefined`] |
| **nativeModerationInput** | [NativeModerationInput](NativeModerationInput.md) |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Moderation accepted |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## removeNativePresenter

> removeNativePresenter(id, userID)

Remove a presenter assignment before the event starts

### Example

```ts
import {
  Configuration,
  NativeMediaApi,
} from '';
import type { RemoveNativePresenterRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NativeMediaApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies RemoveNativePresenterRequest;

  try {
    const data = await api.removeNativePresenter(body);
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
| **userID** | `string` |  | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Presenter removed |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

