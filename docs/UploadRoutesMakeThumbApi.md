# UploadRoutesMakeThumbApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**makeThumb**](UploadRoutesMakeThumbApi.md#makeThumb) | **POST** /api/v1/upload/{id}/make-thumb |  |


<a id="makeThumb"></a>
# **makeThumb**
> FileUploadV2 makeThumb(id)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesMakeThumbApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesMakeThumbApi apiInstance = new UploadRoutesMakeThumbApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      FileUploadV2 result = apiInstance.makeThumb(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesMakeThumbApi#makeThumb");
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
| **200** | Make thumbnail |  -  |

