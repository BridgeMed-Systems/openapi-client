# NativeMediaTransportApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**connectLiveMedia**](NativeMediaTransportApi.md#connectlivemedia) | **GET** /media/livekit/rtc | Connect authorized media WebSocket |
| [**connectLiveMediaV1**](NativeMediaTransportApi.md#connectlivemediav1) | **GET** /media/livekit/rtc/v1 | Connect authorized media WebSocket |
| [**receiveLiveMediaWebhook**](NativeMediaTransportApi.md#receivelivemediawebhook) | **POST** /media/webhooks/livekit | Receive a signed LiveKit lifecycle webhook |
| [**validateLiveMedia**](NativeMediaTransportApi.md#validatelivemedia) | **GET** /media/livekit/rtc/validate | Validate current media admission |
| [**validateLiveMediaV1**](NativeMediaTransportApi.md#validatelivemediav1) | **GET** /media/livekit/rtc/v1/validate | Validate current media admission |



## connectLiveMedia

> connectLiveMedia(accessToken, joinRequest)

Connect authorized media WebSocket

Used by the pinned LiveKit SDK. Requires a signed token and current database admission. Room administration APIs are never proxied. Never log credential-bearing queries.

### Example

```ts
import {
  Configuration,
  NativeMediaTransportApi,
} from '';
import type { ConnectLiveMediaRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new NativeMediaTransportApi();

  const body = {
    // string
    accessToken: accessToken_example,
    // string | Opaque RTC v1 join request. (optional)
    joinRequest: joinRequest_example,
  } satisfies ConnectLiveMediaRequest;

  try {
    const data = await api.connectLiveMedia(body);
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
| **accessToken** | `string` |  | [Defaults to `undefined`] |
| **joinRequest** | `string` | Opaque RTC v1 join request. | [Optional] [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **101** | Media signalling protocol upgrade |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **414** | Query exceeds 64 KiB |  -  |
| **502** | SFU temporarily unreachable |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## connectLiveMediaV1

> connectLiveMediaV1(accessToken, joinRequest)

Connect authorized media WebSocket

Used by the pinned LiveKit SDK. Requires a signed token and current database admission. Room administration APIs are never proxied. Never log credential-bearing queries.

### Example

```ts
import {
  Configuration,
  NativeMediaTransportApi,
} from '';
import type { ConnectLiveMediaV1Request } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new NativeMediaTransportApi();

  const body = {
    // string
    accessToken: accessToken_example,
    // string | Opaque RTC v1 join request. (optional)
    joinRequest: joinRequest_example,
  } satisfies ConnectLiveMediaV1Request;

  try {
    const data = await api.connectLiveMediaV1(body);
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
| **accessToken** | `string` |  | [Defaults to `undefined`] |
| **joinRequest** | `string` | Opaque RTC v1 join request. | [Optional] [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **101** | Media signalling protocol upgrade |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **414** | Query exceeds 64 KiB |  -  |
| **502** | SFU temporarily unreachable |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## receiveLiveMediaWebhook

> receiveLiveMediaWebhook(authorization, requestBody)

Receive a signed LiveKit lifecycle webhook

### Example

```ts
import {
  Configuration,
  NativeMediaTransportApi,
} from '';
import type { ReceiveLiveMediaWebhookRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new NativeMediaTransportApi();

  const body = {
    // string | LiveKit signature containing the raw request body hash.
    authorization: authorization_example,
    // { [key: string]: any; }
    requestBody: Object,
  } satisfies ReceiveLiveMediaWebhookRequest;

  try {
    const data = await api.receiveLiveMediaWebhook(body);
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
| **authorization** | `string` | LiveKit signature containing the raw request body hash. | [Defaults to `undefined`] |
| **requestBody** | `{ [key: string]: any; }` |  | |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/webhook+json`
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Event durably accepted or already received |  -  |
| **401** | Invalid signature or event |  -  |
| **500** | Retryable persistence failure |  -  |
| **503** | Media unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## validateLiveMedia

> validateLiveMedia(accessToken, joinRequest)

Validate current media admission

Used by the pinned LiveKit SDK. Requires a signed token and current database admission. Room administration APIs are never proxied. Never log credential-bearing queries.

### Example

```ts
import {
  Configuration,
  NativeMediaTransportApi,
} from '';
import type { ValidateLiveMediaRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new NativeMediaTransportApi();

  const body = {
    // string
    accessToken: accessToken_example,
    // string | Opaque RTC v1 join request. (optional)
    joinRequest: joinRequest_example,
  } satisfies ValidateLiveMediaRequest;

  try {
    const data = await api.validateLiveMedia(body);
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
| **accessToken** | `string` |  | [Defaults to `undefined`] |
| **joinRequest** | `string` | Opaque RTC v1 join request. | [Optional] [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Admission accepted |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **414** | Query exceeds 64 KiB |  -  |
| **502** | SFU temporarily unreachable |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## validateLiveMediaV1

> validateLiveMediaV1(accessToken, joinRequest)

Validate current media admission

Used by the pinned LiveKit SDK. Requires a signed token and current database admission. Room administration APIs are never proxied. Never log credential-bearing queries.

### Example

```ts
import {
  Configuration,
  NativeMediaTransportApi,
} from '';
import type { ValidateLiveMediaV1Request } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new NativeMediaTransportApi();

  const body = {
    // string
    accessToken: accessToken_example,
    // string | Opaque RTC v1 join request. (optional)
    joinRequest: joinRequest_example,
  } satisfies ValidateLiveMediaV1Request;

  try {
    const data = await api.validateLiveMediaV1(body);
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
| **accessToken** | `string` |  | [Defaults to `undefined`] |
| **joinRequest** | `string` | Opaque RTC v1 join request. | [Optional] [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Admission accepted |  -  |
| **400** | Invalid room request |  -  |
| **401** | Sign in or obtain a current admission |  -  |
| **403** | Room access denied |  -  |
| **404** | Room or participant unavailable |  -  |
| **409** | Seat capacity or room state conflict |  -  |
| **414** | Query exceeds 64 KiB |  -  |
| **502** | SFU temporarily unreachable |  -  |
| **503** | Media service temporarily unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

