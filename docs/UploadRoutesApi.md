# UploadRoutesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteById**](UploadRoutesApi.md#deleteById) | **DELETE** /api/v1/upload/{id} |  |
| [**download**](UploadRoutesApi.md#download) | **GET** /api/v1/upload/download |  |
| [**downloadBulk**](UploadRoutesApi.md#downloadBulk) | **POST** /api/v1/upload/download-bulk |  |
| [**findAllUploads**](UploadRoutesApi.md#findAllUploads) | **GET** /api/v1/upload/find-all |  |
| [**makeThumb**](UploadRoutesApi.md#makeThumb) | **POST** /api/v1/upload/{id}/make-thumb |  |
| [**metadata**](UploadRoutesApi.md#metadata) | **GET** /api/v1/upload/metadata |  |
| [**ping**](UploadRoutesApi.md#ping) | **GET** /api/v1/upload/ping |  |
| [**upload**](UploadRoutesApi.md#upload) | **POST** /api/v1/upload |  |


<a id="deleteById"></a>
# **deleteById**
> deleteById(id)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteById(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#deleteById");
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

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Delete a file by id |  -  |

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
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      File result = apiInstance.download(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#download");
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
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    DownloadBulkRequestUriParams downloadBulkRequestUriParams = new DownloadBulkRequestUriParams(); // DownloadBulkRequestUriParams | 
    try {
      File result = apiInstance.downloadBulk(downloadBulkRequestUriParams);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#downloadBulk");
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

<a id="findAllUploads"></a>
# **findAllUploads**
> List&lt;FileUploadV2&gt; findAllUploads(correlationId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    String correlationId = "correlationId_example"; // String | 
    try {
      List<FileUploadV2> result = apiInstance.findAllUploads(correlationId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#findAllUploads");
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
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      FileUploadV2 result = apiInstance.makeThumb(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#makeThumb");
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
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      FileUploadV2 result = apiInstance.metadata(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#metadata");
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

<a id="ping"></a>
# **ping**
> ping()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    try {
      apiInstance.ping();
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#ping");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ping |  -  |

<a id="upload"></a>
# **upload**
> FileUploadV2 upload(files, correlationId, isPublic, withoutThumbnail)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.UploadRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    UploadRoutesApi apiInstance = new UploadRoutesApi(defaultClient);
    List<File> files = Arrays.asList(); // List<File> | 
    String correlationId = "correlationId_example"; // String | 
    Boolean isPublic = true; // Boolean | 
    Boolean withoutThumbnail = true; // Boolean | 
    try {
      FileUploadV2 result = apiInstance.upload(files, correlationId, isPublic, withoutThumbnail);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UploadRoutesApi#upload");
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

