# EventsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listCalendarEvents**](EventsApi.md#listcalendarevents) | **GET** /v1/events/calendar | Unified calendar events |
| [**listCalendarFeeds**](EventsApi.md#listcalendarfeeds) | **GET** /v1/calendar/feeds | List calendar feeds |
| [**publicCalendarFeed**](EventsApi.md#publiccalendarfeed) | **GET** /calendar/feeds/{scope}/{token}.ics | Public signed calendar feed |
| [**rotateCalendarFeed**](EventsApi.md#rotatecalendarfeedoperation) | **POST** /v1/calendar/feeds/rotate | Rotate calendar feed token |



## listCalendarEvents

> Array&lt;CalendarItem&gt; listCalendarEvents(start, end, scope, types)

Unified calendar events

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { ListCalendarEventsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // Date (optional)
    start: 2013-10-20T19:20:30+01:00,
    // Date (optional)
    end: 2013-10-20T19:20:30+01:00,
    // CalendarScope (optional)
    scope: ...,
    // string | Comma-separated event source types (optional)
    types: types_example,
  } satisfies ListCalendarEventsRequest;

  try {
    const data = await api.listCalendarEvents(body);
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
| **start** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **end** | `Date` |  | [Optional] [Defaults to `undefined`] |
| **scope** | `CalendarScope` |  | [Optional] [Defaults to `undefined`] [Enum: personal, org, hybrid] |
| **types** | `string` | Comma-separated event source types | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;CalendarItem&gt;**](CalendarItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calendar events |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listCalendarFeeds

> Array&lt;CalendarFeed&gt; listCalendarFeeds()

List calendar feeds

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { ListCalendarFeedsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  try {
    const data = await api.listCalendarFeeds();
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

[**Array&lt;CalendarFeed&gt;**](CalendarFeed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calendar feeds |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publicCalendarFeed

> string publicCalendarFeed(scope, token)

Public signed calendar feed

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { PublicCalendarFeedRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new EventsApi();

  const body = {
    // CalendarFeedScope
    scope: ...,
    // string
    token: token_example,
  } satisfies PublicCalendarFeedRequest;

  try {
    const data = await api.publicCalendarFeed(body);
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
| **scope** | `CalendarFeedScope` |  | [Defaults to `undefined`] [Enum: personal, organization] |
| **token** | `string` |  | [Defaults to `undefined`] |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/calendar`, `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | ICS calendar feed |  -  |
| **400** | Validation or request shape error |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## rotateCalendarFeed

> CalendarFeed rotateCalendarFeed(rotateCalendarFeedRequest)

Rotate calendar feed token

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { RotateCalendarFeedOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // RotateCalendarFeedRequest
    rotateCalendarFeedRequest: ...,
  } satisfies RotateCalendarFeedOperationRequest;

  try {
    const data = await api.rotateCalendarFeed(body);
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
| **rotateCalendarFeedRequest** | [RotateCalendarFeedRequest](RotateCalendarFeedRequest.md) |  | |

### Return type

[**CalendarFeed**](CalendarFeed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Calendar feed rotated |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

