# UploadRoutesDownloadBulkApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**downloadBulk**](UploadRoutesDownloadBulkApi.md#downloadBulk) | **POST** /api/v1/upload/download-bulk |  |


<a id="downloadBulk"></a>
# **downloadBulk**
> File downloadBulk(downloadBulkRequestUriParams)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesDownloadBulkApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesDownloadBulkApi apiInstance = new UploadRoutesDownloadBulkApi(defaultClient);
    DownloadBulkRequestUriParams downloadBulkRequestUriParams = new DownloadBulkRequestUriParams(); // DownloadBulkRequestUriParams | 
    try {
      File result = apiInstance.downloadBulk(downloadBulkRequestUriParams);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesDownloadBulkApi#downloadBulk");
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
| **downloadBulkRequestUriParams** | [**DownloadBulkRequestUriParams**](DownloadBulkRequestUriParams.md)|  | |

### Return type

[**File**](File.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Download multiple files as a zip |  -  |

