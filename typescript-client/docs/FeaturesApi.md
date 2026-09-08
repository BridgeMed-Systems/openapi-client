# FeaturesApi

All URIs are relative to *https://api.bridge.med*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getFeatures**](FeaturesApi.md#getfeatures) | **GET** /v1/features | Read integration availability |



## getFeatures

> FeatureSettings getFeatures()

Read integration availability

Public effective integration controls. Contains no provider configuration. Disabled operations return 503 after applicable access checks; authorization and saved records are unchanged.

### Example

```ts
import {
  Configuration,
  FeaturesApi,
} from '';
import type { GetFeaturesRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const api = new FeaturesApi();

  try {
    const data = await api.getFeatures();
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

[**FeatureSettings**](FeatureSettings.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Effective integration settings |  * Cache-Control -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

