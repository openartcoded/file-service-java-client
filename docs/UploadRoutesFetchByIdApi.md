# UploadRoutesFetchByIdApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**download**](UploadRoutesFetchByIdApi.md#download) | **GET** /api/v1/upload/download |  |


<a id="download"></a>
# **download**
> File download(id)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesFetchByIdApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesFetchByIdApi apiInstance = new UploadRoutesFetchByIdApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      File result = apiInstance.download(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesFetchByIdApi#download");
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

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Download file |  -  |

