# CatalogApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCatalogContent**](CatalogApi.md#createcatalogcontentoperation) | **POST** /v1/catalog/content | Create catalog content |
| [**deleteCatalogContent**](CatalogApi.md#deletecatalogcontent) | **DELETE** /v1/catalog/content/{id} | Archive catalog content |
| [**deleteCatalogContentVisibilityPolicy**](CatalogApi.md#deletecatalogcontentvisibilitypolicy) | **DELETE** /v1/catalog/content/policies/{id} | Delete a catalog content visibility policy owned by the authenticated tenant |
| [**getCatalogContent**](CatalogApi.md#getcatalogcontent) | **GET** /v1/catalog/content/{id} | Get catalog content |
| [**listCatalogContent**](CatalogApi.md#listcatalogcontent) | **GET** /v1/catalog/content | List catalog content |
| [**listCatalogContentRecipients**](CatalogApi.md#listcatalogcontentrecipients) | **GET** /v1/catalog/content/{id}/recipients | List eligible catalog content recipient organizations with visibility explanations |
| [**listCatalogContentTags**](CatalogApi.md#listcatalogcontenttags) | **GET** /v1/catalog/content/tags | List catalog content tags |
| [**listCatalogContentVisibilityPolicies**](CatalogApi.md#listcatalogcontentvisibilitypolicies) | **GET** /v1/catalog/content/policies | List catalog content visibility policies for the authenticated hospital or health-system tenant |
| [**publishCatalogContent**](CatalogApi.md#publishcatalogcontent) | **POST** /v1/catalog/content/{id}/publish | Publish catalog content |
| [**revokeCatalogContent**](CatalogApi.md#revokecatalogcontent) | **POST** /v1/catalog/content/{id}/revoke | Revoke catalog content publication |
| [**updateCatalogContent**](CatalogApi.md#updatecatalogcontentoperation) | **PATCH** /v1/catalog/content/{id} | Update catalog content |
| [**upsertCatalogContentVisibilityPolicy**](CatalogApi.md#upsertcatalogcontentvisibilitypolicyoperation) | **PUT** /v1/catalog/content/policies | Upsert an allow/block catalog content visibility policy for the authenticated tenant |
| [**versionCatalogContent**](CatalogApi.md#versioncatalogcontent) | **POST** /v1/catalog/content/{id}/version | Bump catalog content publication version |



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


## deleteCatalogContentVisibilityPolicy

> deleteCatalogContentVisibilityPolicy(id)

Delete a catalog content visibility policy owned by the authenticated tenant

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { DeleteCatalogContentVisibilityPolicyRequest } from '';

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
  } satisfies DeleteCatalogContentVisibilityPolicyRequest;

  try {
    const data = await api.deleteCatalogContentVisibilityPolicy(body);
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
| **204** | Catalog content visibility policy deleted |  -  |
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


## listCatalogContentRecipients

> Array&lt;CatalogContentRecipient&gt; listCatalogContentRecipients(id)

List eligible catalog content recipient organizations with visibility explanations

Vendor admins for the owning vendor organization, and platform admins, can see hospital/health-system recipient organizations derived from product assignments or explicit visibility policies. The response is organization-level only and does not include staff assignments or user activity.

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { ListCatalogContentRecipientsRequest } from '';

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
  } satisfies ListCatalogContentRecipientsRequest;

  try {
    const data = await api.listCatalogContentRecipients(body);
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

[**Array&lt;CatalogContentRecipient&gt;**](CatalogContentRecipient.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content recipient visibility explanations |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
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


## listCatalogContentVisibilityPolicies

> Array&lt;CatalogContentVisibilityPolicy&gt; listCatalogContentVisibilityPolicies()

List catalog content visibility policies for the authenticated hospital or health-system tenant

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { ListCatalogContentVisibilityPoliciesRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  try {
    const data = await api.listCatalogContentVisibilityPolicies();
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

[**Array&lt;CatalogContentVisibilityPolicy&gt;**](CatalogContentVisibilityPolicy.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content visibility policies |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## publishCatalogContent

> CatalogContentItem publishCatalogContent(id)

Publish catalog content

Vendor admins for the owning vendor organization, and platform admins, can publish catalog content. Publishing sets publication_status to published, sets date_published, and clears date_revoked.

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { PublishCatalogContentRequest } from '';

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
  } satisfies PublishCatalogContentRequest;

  try {
    const data = await api.publishCatalogContent(body);
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


## revokeCatalogContent

> CatalogContentItem revokeCatalogContent(id)

Revoke catalog content publication

Vendor admins for the owning vendor organization, and platform admins, can revoke catalog content. Revocation sets publication_status to revoked and date_revoked.

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { RevokeCatalogContentRequest } from '';

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
  } satisfies RevokeCatalogContentRequest;

  try {
    const data = await api.revokeCatalogContent(body);
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


## upsertCatalogContentVisibilityPolicy

> CatalogContentVisibilityPolicy upsertCatalogContentVisibilityPolicy(upsertCatalogContentVisibilityPolicyRequest)

Upsert an allow/block catalog content visibility policy for the authenticated tenant

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { UpsertCatalogContentVisibilityPolicyOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CatalogApi(config);

  const body = {
    // UpsertCatalogContentVisibilityPolicyRequest
    upsertCatalogContentVisibilityPolicyRequest: ...,
  } satisfies UpsertCatalogContentVisibilityPolicyOperationRequest;

  try {
    const data = await api.upsertCatalogContentVisibilityPolicy(body);
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
| **upsertCatalogContentVisibilityPolicyRequest** | [UpsertCatalogContentVisibilityPolicyRequest](UpsertCatalogContentVisibilityPolicyRequest.md) |  | |

### Return type

[**CatalogContentVisibilityPolicy**](CatalogContentVisibilityPolicy.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Catalog content visibility policy |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## versionCatalogContent

> CatalogContentItem versionCatalogContent(id)

Bump catalog content publication version

Vendor admins for the owning vendor organization, and platform admins, can increment publication_version. This action does not publish or revoke content; it preserves the current publication_status and updates date_updated.

### Example

```ts
import {
  Configuration,
  CatalogApi,
} from '';
import type { VersionCatalogContentRequest } from '';

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
  } satisfies VersionCatalogContentRequest;

  try {
    const data = await api.versionCatalogContent(body);
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

