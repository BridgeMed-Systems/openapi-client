# EventsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelEventRegistration**](EventsApi.md#canceleventregistration) | **DELETE** /v1/events/{type}/{id}/registrations/me | Cancel your pending event registration |
| [**exportCalendarEvent**](EventsApi.md#exportcalendarevent) | **GET** /v1/events/{type}/{id}/calendar.ics | Export one authorized education event |
| [**listCalendarEvents**](EventsApi.md#listcalendarevents) | **GET** /v1/events/calendar | Unified calendar events |
| [**listCalendarFeeds**](EventsApi.md#listcalendarfeeds) | **GET** /v1/calendar/feeds | List calendar feeds |
| [**listEventRegistrations**](EventsApi.md#listeventregistrations) | **GET** /v1/events/{type}/{id}/registrations | Read private hospital event registrations |
| [**publicCalendarFeed**](EventsApi.md#publiccalendarfeed) | **GET** /calendar/feeds/{scope}/{token}.ics | Private bearer calendar subscription |
| [**recordEventAttendance**](EventsApi.md#recordeventattendanceoperation) | **PATCH** /v1/events/{type}/{id}/registrations/{userID} | Record a hospital learner attendance outcome with evidence |
| [**registerForEvent**](EventsApi.md#registerforevent) | **POST** /v1/events/{type}/{id}/registrations/me | Register yourself for an education event |
| [**revokeCalendarFeed**](EventsApi.md#revokecalendarfeed) | **POST** /v1/calendar/feeds/revoke | Stop a private calendar subscription |
| [**rotateCalendarFeed**](EventsApi.md#rotatecalendarfeedoperation) | **POST** /v1/calendar/feeds/rotate | Rotate calendar feed token |



## cancelEventRegistration

> cancelEventRegistration(type, id)

Cancel your pending event registration

Hospital learners read their own records; hospital administrators read only their hospital. Vendor and human platform roles have no access. Registration does not prove attendance or award credit.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { CancelEventRegistrationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // 'training' | 'webinar'
    type: type_example,
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CancelEventRegistrationRequest;

  try {
    const data = await api.cancelEventRegistration(body);
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
| **type** | `training`, `webinar` |  | [Defaults to `undefined`] [Enum: training, webinar] |
| **id** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Pending registration cancelled or already absent |  -  |
| **400** | Invalid event or attendance evidence |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital learning permission required |  -  |
| **404** | Event or private record unavailable |  -  |
| **409** | Event full or attendance already recorded |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## exportCalendarEvent

> Blob exportCalendarEvent(type, id)

Export one authorized education event

Private iCalendar download with the same stable UID, update sequence and cancellation status as subscriptions. Exporting is not registration or attendance.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { ExportCalendarEventRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // 'webinar' | 'training'
    type: type_example,
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ExportCalendarEventRequest;

  try {
    const data = await api.exportCalendarEvent(body);
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
| **type** | `webinar`, `training` |  | [Defaults to `undefined`] [Enum: webinar, training] |
| **id** | `string` |  | [Defaults to `undefined`] |

### Return type

**Blob**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/calendar`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Individual event |  -  |
| **400** | Invalid calendar request |  -  |
| **401** | Sign in required |  -  |
| **403** | Current calendar access required |  -  |
| **404** | Event unavailable in this organization |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


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


## listEventRegistrations

> Array&lt;TrainingSessionRegistration&gt; listEventRegistrations(type, id)

Read private hospital event registrations

Hospital learners read their own records; hospital administrators read only their hospital. Vendor and human platform roles have no access. Registration does not prove attendance or award credit.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { ListEventRegistrationsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // 'training' | 'webinar'
    type: type_example,
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListEventRegistrationsRequest;

  try {
    const data = await api.listEventRegistrations(body);
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
| **type** | `training`, `webinar` |  | [Defaults to `undefined`] [Enum: training, webinar] |
| **id** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Array&lt;TrainingSessionRegistration&gt;**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Private event participation |  -  |
| **400** | Invalid event or attendance evidence |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital learning permission required |  -  |
| **404** | Event or private record unavailable |  -  |
| **409** | Event full or attendance already recorded |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publicCalendarFeed

> string publicCalendarFeed(scope, token)

Private bearer calendar subscription

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
| **200** | Private iCalendar subscription. Stable UIDs, revision sequences, UTC times and cancellation records. Provider refresh timing varies. |  -  |
| **400** | Validation or request shape error |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## recordEventAttendance

> TrainingSessionRegistration recordEventAttendance(type, id, userID, recordEventAttendanceRequest)

Record a hospital learner attendance outcome with evidence

Hospital learners read their own records; hospital administrators read only their hospital. Vendor and human platform roles have no access. Registration does not prove attendance or award credit.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { RecordEventAttendanceOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // 'training' | 'webinar'
    type: type_example,
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // RecordEventAttendanceRequest
    recordEventAttendanceRequest: ...,
  } satisfies RecordEventAttendanceOperationRequest;

  try {
    const data = await api.recordEventAttendance(body);
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
| **type** | `training`, `webinar` |  | [Defaults to `undefined`] [Enum: training, webinar] |
| **id** | `string` |  | [Defaults to `undefined`] |
| **userID** | `string` |  | [Defaults to `undefined`] |
| **recordEventAttendanceRequest** | [RecordEventAttendanceRequest](RecordEventAttendanceRequest.md) |  | |

### Return type

[**TrainingSessionRegistration**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Private event participation |  -  |
| **400** | Invalid event or attendance evidence |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital learning permission required |  -  |
| **404** | Event or private record unavailable |  -  |
| **409** | Event full or attendance already recorded |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## registerForEvent

> TrainingSessionRegistration registerForEvent(type, id)

Register yourself for an education event

Hospital learners read their own records; hospital administrators read only their hospital. Vendor and human platform roles have no access. Registration does not prove attendance or award credit.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { RegisterForEventRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new EventsApi(config);

  const body = {
    // 'training' | 'webinar'
    type: type_example,
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies RegisterForEventRequest;

  try {
    const data = await api.registerForEvent(body);
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
| **type** | `training`, `webinar` |  | [Defaults to `undefined`] [Enum: training, webinar] |
| **id** | `string` |  | [Defaults to `undefined`] |

### Return type

[**TrainingSessionRegistration**](TrainingSessionRegistration.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Private event participation |  -  |
| **400** | Invalid event or attendance evidence |  -  |
| **401** | Sign in required |  -  |
| **403** | Hospital learning permission required |  -  |
| **404** | Event or private record unavailable |  -  |
| **409** | Event full or attendance already recorded |  -  |
| **500** | Server failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## revokeCalendarFeed

> revokeCalendarFeed(rotateCalendarFeedRequest)

Stop a private calendar subscription

Immediately rejects the old URL. Listing subscriptions preserves the stopped state. Rotate explicitly to create a replacement URL.

### Example

```ts
import {
  Configuration,
  EventsApi,
} from '';
import type { RevokeCalendarFeedRequest } from '';

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
  } satisfies RevokeCalendarFeedRequest;

  try {
    const data = await api.revokeCalendarFeed(body);
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

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Subscription stopped |  -  |
| **400** | Invalid calendar request |  -  |
| **401** | Sign in required |  -  |
| **403** | Current calendar access required |  -  |
| **404** | Event unavailable in this organization |  -  |
| **500** | Server failure |  -  |

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

