# UploadRoutesMetadataApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**metadata**](UploadRoutesMetadataApi.md#metadata) | **GET** /api/v1/upload/metadata |  |


<a id="metadata"></a>
# **metadata**
> FileUploadV2 metadata(id)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesMetadataApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesMetadataApi apiInstance = new UploadRoutesMetadataApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      FileUploadV2 result = apiInstance.metadata(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesMetadataApi#metadata");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | **String**|  | |

### Return type

[**FileUploadV2**](FileUploadV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Get upload metadata |  -  |

