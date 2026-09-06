# DocumentsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**addDocumentRevision**](DocumentsApi.md#adddocumentrevision) | **POST** /v1/documents/{id}/revisions | Create or resume a draft with identical metadata |
| [**confirmVideoUpload**](DocumentsApi.md#confirmvideoupload) | **POST** /v1/videos/{id}/upload-complete | Confirm a complete source upload |
| [**createManagedDocument**](DocumentsApi.md#createmanageddocumentoperation) | **POST** /v1/documents/ | Create a private document and draft revision |
| [**createVideo**](DocumentsApi.md#createvideooperation) | **POST** /v1/videos/ | Create a private video and draft revision |
| [**getDocumentAsset**](DocumentsApi.md#getdocumentasset) | **GET** /v1/documents/{id}/revisions/{revision}/assets/{name} | Authorize and deliver a private document asset |
| [**getManagedDocument**](DocumentsApi.md#getmanageddocument) | **GET** /v1/documents/{id} | Get a document and its permitted revisions |
| [**getVideo**](DocumentsApi.md#getvideo) | **GET** /v1/videos/{id} | Read authorized video metadata |
| [**getVideoPlayback**](DocumentsApi.md#getvideoplayback) | **GET** /v1/videos/{id}/play | Resolve authenticated video playback |
| [**headDocumentAsset**](DocumentsApi.md#headdocumentasset) | **HEAD** /v1/documents/{id}/revisions/{revision}/assets/{name} | Authorize and deliver a private document asset |
| [**listManagedDocuments**](DocumentsApi.md#listmanageddocuments) | **GET** /v1/documents/ | List private documents for a device |
| [**publishDocumentRevision**](DocumentsApi.md#publishdocumentrevision) | **POST** /v1/documents/{id}/revisions/{revision}/publish | Publish a validated revision to eligible libraries |
| [**retryDocumentProcessing**](DocumentsApi.md#retrydocumentprocessing) | **POST** /v1/documents/{id}/revisions/{revision}/retry | Request processing retry for a failed draft |
| [**setDocumentHospitalVisibility**](DocumentsApi.md#setdocumenthospitalvisibility) | **PUT** /v1/documents/{id}/visibility | Set visibility in the current hospital library |
| [**uploadDocumentSource**](DocumentsApi.md#uploaddocumentsource) | **PUT** /v1/documents/{id}/revisions/{revision}/source | Upload source bytes for validation and processing |
| [**withdrawDocumentRevision**](DocumentsApi.md#withdrawdocumentrevision) | **POST** /v1/documents/{id}/revisions/{revision}/withdraw | Withdraw a revision and invalidate its delivery |



## addDocumentRevision

> DocumentRevision addDocumentRevision(id, documentRevisionInput)

Create or resume a draft with identical metadata

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { AddDocumentRevisionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // DocumentRevisionInput
    documentRevisionInput: ...,
  } satisfies AddDocumentRevisionRequest;

  try {
    const data = await api.addDocumentRevision(body);
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
| **documentRevisionInput** | [DocumentRevisionInput](DocumentRevisionInput.md) |  | |

### Return type

[**DocumentRevision**](DocumentRevision.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Create or resume a draft with identical metadata |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## confirmVideoUpload

> confirmVideoUpload(id, videoUploadConfirmation)

Confirm a complete source upload

Upload through the document source endpoint first. It verifies the bytes and queues processing atomically. This idempotent confirmation cannot accept an incomplete source.

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { ConfirmVideoUploadRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // VideoUploadConfirmation
    videoUploadConfirmation: ...,
  } satisfies ConfirmVideoUploadRequest;

  try {
    const data = await api.confirmVideoUpload(body);
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
| **videoUploadConfirmation** | [VideoUploadConfirmation](VideoUploadConfirmation.md) |  | |

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
| **202** | Uploaded file is queued, processing or ready. |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createManagedDocument

> ManagedDocument createManagedDocument(idempotencyKey, createManagedDocumentRequest)

Create a private document and draft revision

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { CreateManagedDocumentOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string | Reuse the same UUID only for an identical submission.
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateManagedDocumentRequest
    createManagedDocumentRequest: ...,
  } satisfies CreateManagedDocumentOperationRequest;

  try {
    const data = await api.createManagedDocument(body);
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
| **idempotencyKey** | `string` | Reuse the same UUID only for an identical submission. | [Defaults to `undefined`] |
| **createManagedDocumentRequest** | [CreateManagedDocumentRequest](CreateManagedDocumentRequest.md) |  | |

### Return type

[**ManagedDocument**](ManagedDocument.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Create a private document and draft revision |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createVideo

> ManagedDocument createVideo(idempotencyKey, createVideoRequest)

Create a private video and draft revision

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { CreateVideoOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    idempotencyKey: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateVideoRequest
    createVideoRequest: ...,
  } satisfies CreateVideoOperationRequest;

  try {
    const data = await api.createVideo(body);
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
| **createVideoRequest** | [CreateVideoRequest](CreateVideoRequest.md) |  | |

### Return type

[**ManagedDocument**](ManagedDocument.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Create a private video and draft revision |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getDocumentAsset

> Blob getDocumentAsset(id, revision, name, range, download)

Authorize and deliver a private document asset

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { GetDocumentAssetRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    name: name_example,
    // string | One bytes range. Multiple ranges are rejected. (optional)
    range: range_example,
    // '1' (optional)
    download: download_example,
  } satisfies GetDocumentAssetRequest;

  try {
    const data = await api.getDocumentAsset(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |
| **name** | `string` |  | [Defaults to `undefined`] |
| **range** | `string` | One bytes range. Multiple ranges are rejected. | [Optional] [Defaults to `undefined`] |
| **download** | `1` |  | [Optional] [Defaults to `undefined`] [Enum: 1] |

### Return type

**Blob**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `image/png`, `image/jpeg`, `application/vnd.apple.mpegurl`, `video/mp2t`, `text/vtt`, `application/octet-stream`, `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Authorize and deliver a private document asset |  * Content-Length -  <br>  * Accept-Ranges -  <br>  |
| **206** | Authorized byte range |  * Content-Range -  <br>  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **416** | Requested range cannot be satisfied |  * Content-Range -  <br>  |
| **500** | Internal server error |  -  |
| **503** | Temporary storage failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getManagedDocument

> ManagedDocument getManagedDocument(id)

Get a document and its permitted revisions

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { GetManagedDocumentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetManagedDocumentRequest;

  try {
    const data = await api.getManagedDocument(body);
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

[**ManagedDocument**](ManagedDocument.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Get a document and its permitted revisions |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getVideo

> ManagedDocument getVideo(id)

Read authorized video metadata

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { GetVideoRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetVideoRequest;

  try {
    const data = await api.getVideo(body);
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

[**ManagedDocument**](ManagedDocument.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Read authorized video metadata |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getVideoPlayback

> VideoPlayback getVideoPlayback(id, revisionId)

Resolve authenticated video playback

Every manifest, caption and segment request requires a valid short-lived signed application session and live tenant authorization. URLs contain no bearer secrets.

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { GetVideoPlaybackRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    revisionId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetVideoPlaybackRequest;

  try {
    const data = await api.getVideoPlayback(body);
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
| **revisionId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**VideoPlayback**](VideoPlayback.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Resolve authenticated video playback |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## headDocumentAsset

> headDocumentAsset(id, revision, name, range, download)

Authorize and deliver a private document asset

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { HeadDocumentAssetRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    name: name_example,
    // string | One bytes range. Multiple ranges are rejected. (optional)
    range: range_example,
    // '1' (optional)
    download: download_example,
  } satisfies HeadDocumentAssetRequest;

  try {
    const data = await api.headDocumentAsset(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |
| **name** | `string` |  | [Defaults to `undefined`] |
| **range** | `string` | One bytes range. Multiple ranges are rejected. | [Optional] [Defaults to `undefined`] |
| **download** | `1` |  | [Optional] [Defaults to `undefined`] [Enum: 1] |

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
| **200** | Authorize and deliver a private document asset |  * Content-Length -  <br>  * Accept-Ranges -  <br>  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **416** | Requested range cannot be satisfied |  * Content-Range -  <br>  |
| **500** | Internal server error |  -  |
| **503** | Temporary storage failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listManagedDocuments

> ManagedDocumentPage listManagedDocuments(productId, limit, offset)

List private documents for a device

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { ListManagedDocumentsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    productId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies ListManagedDocumentsRequest;

  try {
    const data = await api.listManagedDocuments(body);
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
| **productId** | `string` |  | [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**ManagedDocumentPage**](ManagedDocumentPage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List private documents for a device |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publishDocumentRevision

> publishDocumentRevision(id, revision)

Publish a validated revision to eligible libraries

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { PublishDocumentRevisionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies PublishDocumentRevisionRequest;

  try {
    const data = await api.publishDocumentRevision(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Publish a validated revision to eligible libraries |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## retryDocumentProcessing

> retryDocumentProcessing(id, revision)

Request processing retry for a failed draft

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { RetryDocumentProcessingRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies RetryDocumentProcessingRequest;

  try {
    const data = await api.retryDocumentProcessing(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |

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
| **202** | Request processing retry for a failed draft |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## setDocumentHospitalVisibility

> setDocumentHospitalVisibility(id, documentVisibilityRequest)

Set visibility in the current hospital library

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { SetDocumentHospitalVisibilityRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // DocumentVisibilityRequest
    documentVisibilityRequest: ...,
  } satisfies SetDocumentHospitalVisibilityRequest;

  try {
    const data = await api.setDocumentHospitalVisibility(body);
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
| **documentVisibilityRequest** | [DocumentVisibilityRequest](DocumentVisibilityRequest.md) |  | |

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
| **204** | Set visibility in the current hospital library |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## uploadDocumentSource

> uploadDocumentSource(id, revision, body)

Upload source bytes for validation and processing

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { UploadDocumentSourceRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // Blob
    body: BINARY_DATA_HERE,
  } satisfies UploadDocumentSourceRequest;

  try {
    const data = await api.uploadDocumentSource(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |
| **body** | `Blob` |  | |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/octet-stream`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Upload source bytes for validation and processing |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |
| **503** | Temporary storage failure |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## withdrawDocumentRevision

> withdrawDocumentRevision(id, revision, documentWithdrawalRequest)

Withdraw a revision and invalidate its delivery

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { WithdrawDocumentRevisionRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    revision: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // DocumentWithdrawalRequest
    documentWithdrawalRequest: ...,
  } satisfies WithdrawDocumentRevisionRequest;

  try {
    const data = await api.withdrawDocumentRevision(body);
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
| **revision** | `string` |  | [Defaults to `undefined`] |
| **documentWithdrawalRequest** | [DocumentWithdrawalRequest](DocumentWithdrawalRequest.md) |  | |

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
| **204** | Withdraw a revision and invalidate its delivery |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

