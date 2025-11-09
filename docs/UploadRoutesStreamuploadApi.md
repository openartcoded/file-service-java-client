# UploadRoutesStreamuploadApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**upload**](UploadRoutesStreamuploadApi.md#upload) | **POST** /api/v1/upload |  |


<a id="upload"></a>
# **upload**
> List&lt;FileUploadV2&gt; upload(files, correlationId, isPublic, withoutThumbnail)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesStreamuploadApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesStreamuploadApi apiInstance = new UploadRoutesStreamuploadApi(defaultClient);
    List<File> files = Arrays.asList(); // List<File> | 
    String correlationId = "correlationId_example"; // String | 
    Boolean isPublic = true; // Boolean | 
    Boolean withoutThumbnail = true; // Boolean | 
    try {
      List<FileUploadV2> result = apiInstance.upload(files, correlationId, isPublic, withoutThumbnail);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesStreamuploadApi#upload");
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
| **files** | **List&lt;File&gt;**|  | |
| **correlationId** | **String**|  | [optional] |
| **isPublic** | **Boolean**|  | [optional] |
| **withoutThumbnail** | **Boolean**|  | [optional] |

### Return type

[**List&lt;FileUploadV2&gt;**](FileUploadV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upload a file |  -  |

