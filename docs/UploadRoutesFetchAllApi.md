# UploadRoutesFetchAllApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**findAll**](UploadRoutesFetchAllApi.md#findAll) | **GET** /api/v1/upload/find-all |  |


<a id="findAll"></a>
# **findAll**
> List&lt;FileUploadV2&gt; findAll(correlationId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesFetchAllApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesFetchAllApi apiInstance = new UploadRoutesFetchAllApi(defaultClient);
    String correlationId = "correlationId_example"; // String | 
    try {
      List<FileUploadV2> result = apiInstance.findAll(correlationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesFetchAllApi#findAll");
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
| **correlationId** | **String**|  | [optional] |

### Return type

[**List&lt;FileUploadV2&gt;**](FileUploadV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find all upload |  -  |

