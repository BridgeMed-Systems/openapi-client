# ProductsApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProduct**](ProductsApi.md#createproductoperation) | **POST** /v1/products | Create product |
| [**createProductOrganization**](ProductsApi.md#createproductorganizationoperation) | **POST** /v1/products/{id}/organizations | Add organization to product |
| [**createProductUser**](ProductsApi.md#createproductuseroperation) | **POST** /v1/products/{id}/users | Add user to product |
| [**deleteProductOrganization**](ProductsApi.md#deleteproductorganization) | **DELETE** /v1/products/{id}/organizations/{organizationID} | Remove organization from product |
| [**deleteProductUser**](ProductsApi.md#deleteproductuser) | **DELETE** /v1/products/{id}/users/{userID} | Remove user from product |
| [**getProduct**](ProductsApi.md#getproduct) | **GET** /v1/products/{id} | Get product |
| [**listProductOrganizations**](ProductsApi.md#listproductorganizations) | **GET** /v1/products/{id}/organizations | List product organizations |
| [**listProductUsers**](ProductsApi.md#listproductusers) | **GET** /v1/products/{id}/users | List product users |
| [**listProducts**](ProductsApi.md#listproducts) | **GET** /v1/products | List products |
| [**searchDevices**](ProductsApi.md#searchdevices) | **GET** /v1/products/search | Search visible devices with direct document actions |
| [**updateProductMetadata**](ProductsApi.md#updateproductmetadataoperation) | **PUT** /v1/products/{id} | Update owned product catalog details using the current revision |



## createProduct

> Product createProduct(createProductRequest)

Create product

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { CreateProductOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // CreateProductRequest
    createProductRequest: ...,
  } satisfies CreateProductOperationRequest;

  try {
    const data = await api.createProduct(body);
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
| **createProductRequest** | [CreateProductRequest](CreateProductRequest.md) |  | |

### Return type

[**Product**](Product.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createProductOrganization

> ProductOrganization createProductOrganization(id, createProductOrganizationRequest)

Add organization to product

Representative callers can only assign products already assigned to themselves and only to directly supported hospital or health_system organizations.

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { CreateProductOrganizationOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateProductOrganizationRequest
    createProductOrganizationRequest: ...,
  } satisfies CreateProductOrganizationOperationRequest;

  try {
    const data = await api.createProductOrganization(body);
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
| **createProductOrganizationRequest** | [CreateProductOrganizationRequest](CreateProductOrganizationRequest.md) |  | |

### Return type

[**ProductOrganization**](ProductOrganization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product organization created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createProductUser

> UserProduct createProductUser(id, createProductUserRequest)

Add user to product

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { CreateProductUserOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // CreateProductUserRequest
    createProductUserRequest: ...,
  } satisfies CreateProductUserOperationRequest;

  try {
    const data = await api.createProductUser(body);
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
| **createProductUserRequest** | [CreateProductUserRequest](CreateProductUserRequest.md) |  | |

### Return type

[**UserProduct**](UserProduct.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Product user created |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteProductOrganization

> deleteProductOrganization(id, organizationID)

Remove organization from product

Representative callers can only remove assignments for products already assigned to themselves and only from directly supported hospital or health_system organizations.

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { DeleteProductOrganizationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    organizationID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeleteProductOrganizationRequest;

  try {
    const data = await api.deleteProductOrganization(body);
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
| **organizationID** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Product organization removed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deleteProductUser

> deleteProductUser(id, userID)

Remove user from product

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { DeleteProductUserRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string
    userID: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeleteProductUserRequest;

  try {
    const data = await api.deleteProductUser(body);
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
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Product user removed |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getProduct

> Product getProduct(id)

Get product

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { GetProductRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetProductRequest;

  try {
    const data = await api.getProduct(body);
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

[**Product**](Product.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listProductOrganizations

> Array&lt;ProductOrganization&gt; listProductOrganizations(id)

List product organizations

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { ListProductOrganizationsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListProductOrganizationsRequest;

  try {
    const data = await api.listProductOrganizations(body);
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

[**Array&lt;ProductOrganization&gt;**](ProductOrganization.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product organizations |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listProductUsers

> Array&lt;UserProduct&gt; listProductUsers(id)

List product users

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { ListProductUsersRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies ListProductUsersRequest;

  try {
    const data = await api.listProductUsers(body);
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

[**Array&lt;UserProduct&gt;**](UserProduct.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Product users |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listProducts

> Array&lt;Product&gt; listProducts(scope)

List products

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { ListProductsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // 'assigned' | 'assigned_organization' (optional)
    scope: scope_example,
  } satisfies ListProductsRequest;

  try {
    const data = await api.listProducts(body);
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
| **scope** | `assigned`, `assigned_organization` |  | [Optional] [Defaults to `undefined`] [Enum: assigned, assigned_organization] |

### Return type

[**Array&lt;Product&gt;**](Product.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Products |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## searchDevices

> DeviceSearchResult searchDevices(q, vendorId, specialty, procedureType, libraryScope, limit, offset)

Search visible devices with direct document actions

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { SearchDevicesRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string (optional)
    q: q_example,
    // string (optional)
    vendorId: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // string (optional)
    specialty: specialty_example,
    // string (optional)
    procedureType: procedureType_example,
    // 'selected' | 'available' | Available requires hospital library management. (optional)
    libraryScope: libraryScope_example,
    // number (optional)
    limit: 56,
    // number (optional)
    offset: 56,
  } satisfies SearchDevicesRequest;

  try {
    const data = await api.searchDevices(body);
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
| **vendorId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **specialty** | `string` |  | [Optional] [Defaults to `undefined`] |
| **procedureType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **libraryScope** | `selected`, `available` | Available requires hospital library management. | [Optional] [Defaults to `&#39;selected&#39;`] [Enum: selected, available] |
| **limit** | `number` |  | [Optional] [Defaults to `30`] |
| **offset** | `number` |  | [Optional] [Defaults to `0`] |

### Return type

[**DeviceSearchResult**](DeviceSearchResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Tenant-scoped device results and filter choices |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## updateProductMetadata

> Product updateProductMetadata(id, updateProductMetadataRequest)

Update owned product catalog details using the current revision

### Example

```ts
import {
  Configuration,
  ProductsApi,
} from '';
import type { UpdateProductMetadataOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ProductsApi(config);

  const body = {
    // string
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // UpdateProductMetadataRequest
    updateProductMetadataRequest: ...,
  } satisfies UpdateProductMetadataOperationRequest;

  try {
    const data = await api.updateProductMetadata(body);
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
| **updateProductMetadataRequest** | [UpdateProductMetadataRequest](UpdateProductMetadataRequest.md) |  | |

### Return type

[**Product**](Product.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated product details |  -  |
| **400** | Validation or request shape error |  -  |
| **401** | Missing or invalid authentication |  -  |
| **403** | Authenticated caller is not allowed to perform this action |  -  |
| **404** | Resource not found |  -  |
| **409** | Conflict with existing state |  -  |
| **500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

