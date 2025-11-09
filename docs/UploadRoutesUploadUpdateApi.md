# UploadRoutesUploadUpdateApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**uploadUpdate**](UploadRoutesUploadUpdateApi.md#uploadUpdate) | **POST** /api/v1/upload/{id}/update |  |


<a id="uploadUpdate"></a>
# **uploadUpdate**
> FileUploadV2 uploadUpdate(id, files)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesUploadUpdateApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesUploadUpdateApi apiInstance = new UploadRoutesUploadUpdateApi(defaultClient);
    String id = "id_example"; // String | 
    File files = new File("/path/to/file"); // File | 
    try {
      FileUploadV2 result = apiInstance.uploadUpdate(id, files);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesUploadUpdateApi#uploadUpdate");
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
| **files** | **File**|  | |

### Return type

[**FileUploadV2**](FileUploadV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upload a file |  -  |

