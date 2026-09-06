# CatalogApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCatalogContent**](CatalogApi.md#createcatalogcontentoperation) | **POST** /v1/catalog/content | Create catalog content |
| [**deleteCatalogContent**](CatalogApi.md#deletecatalogcontent) | **DELETE** /v1/catalog/content/{id} | Archive catalog content |
| [**getCatalogContent**](CatalogApi.md#getcatalogcontent) | **GET** /v1/catalog/content/{id} | Get catalog content |
| [**listCatalogContent**](CatalogApi.md#listcatalogcontent) | **GET** /v1/catalog/content | List catalog content |
| [**listCatalogContentTags**](CatalogApi.md#listcatalogcontenttags) | **GET** /v1/catalog/content/tags | List catalog content tags |
| [**updateCatalogContent**](CatalogApi.md#updatecatalogcontentoperation) | **PATCH** /v1/catalog/content/{id} | Update catalog content |



## createCatalogContent

> CatalogContentItem createCatalogContent(createCatalogContentRequest)

Create catalog content

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { CreateCatalogContentOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // CreateCatalogContentRequest
    createCatalogContentRequest: ...,
  } satisfies CreateCatalogContentOperationRequest;

  try {
    const data = await api.createCatalogContent(body);
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
| **createCatalogContentRequest** | [CreateCatalogContentRequest](CreateCatalogContentRequest.md) |  | |

### Return type

[**CatalogContentItem**](CatalogContentItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Catalog content created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteCatalogContent

> deleteCatalogContent(id)

Archive catalog content

Archives legacy external material with catalog.content.withdraw. It does not delete the record; managed documents use revision withdrawal. Current vendor ownership and explicit denies are rechecked, and the archive is audited atomically.

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { DeleteCatalogContentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeleteCatalogContentRequest;

  try {
    const data = await api.deleteCatalogContent(body);
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
| **204** | Catalog content archived |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getCatalogContent

> CatalogContentItem getCatalogContent(id)

Get catalog content

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { GetCatalogContentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetCatalogContentRequest;

  try {
    const data = await api.getCatalogContent(body);
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

[**CatalogContentItem**](CatalogContentItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content item |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listCatalogContent

> Array&lt;CatalogContentItem&gt; listCatalogContent(q, organizationId, productId, includeArchived, types, tags)

List catalog content

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { ListCatalogContentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    organizationId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    productId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // boolean (optional)
    includeArchived: true,
    // string | Comma-separated content types (optional)
    types: types_example,
    // string | Comma-separated content tags (optional)
    tags: tags_example,
  } satisfies ListCatalogContentRequest;

  try {
    const data = await api.listCatalogContent(body);
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
| **organizationId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **productId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **includeArchived** | `boolean` |  | [Optional] [Defaults to `undefined`] |
| **types** | `string` | Comma-separated content types | [Optional] [Defaults to `undefined`] |
| **tags** | `string` | Comma-separated content tags | [Optional] [Defaults to `undefined`] |

### Return type

[**Array&lt;CatalogContentItem&gt;**](CatalogContentItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content items |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listCatalogContentTags

> Array&lt;string&gt; listCatalogContentTags()

List catalog content tags

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { ListCatalogContentTagsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  try {
    const data = await api.listCatalogContentTags();
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

**Array<string>**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content tags |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateCatalogContent

> CatalogContentItem updateCatalogContent(id, updateCatalogContentRequest)

Update catalog content

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { UpdateCatalogContentOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateCatalogContentRequest
    updateCatalogContentRequest: ...,
  } satisfies UpdateCatalogContentOperationRequest;

  try {
    const data = await api.updateCatalogContent(body);
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
| **updateCatalogContentRequest** | [UpdateCatalogContentRequest](UpdateCatalogContentRequest.md) |  | |

### Return type

[**CatalogContentItem**](CatalogContentItem.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content item |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

