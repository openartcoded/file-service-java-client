# TemplateRoutesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteTemplById**](TemplateRoutesApi.md#deleteTemplById) | **DELETE** /api/v1/template/{id} |  |
| [**findAll**](TemplateRoutesApi.md#findAll) | **GET** /api/v1/template/find-all |  |
| [**findByContext**](TemplateRoutesApi.md#findByContext) | **GET** /api/v1/template/find-by-context |  |
| [**findByIds**](TemplateRoutesApi.md#findByIds) | **GET** /api/v1/template/find-by-ids |  |
| [**findByType**](TemplateRoutesApi.md#findByType) | **GET** /api/v1/template/find-by-type |  |
| [**findOne**](TemplateRoutesApi.md#findOne) | **GET** /api/v1/template/find-one/{templ_id} |  |
| [**render**](TemplateRoutesApi.md#render) | **POST** /api/v1/template/render |  |
| [**upsert**](TemplateRoutesApi.md#upsert) | **POST** /api/v1/template |  |


<a id="deleteTemplById"></a>
# **deleteTemplById**
> deleteTemplById(id)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    String id = "id_example"; // String | 
    try {
      apiInstance.deleteTemplById(id);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#deleteTemplById");
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
| **200** | Delete a template by id |  -  |

<a id="findAll"></a>
# **findAll**
> List&lt;TemplateV2&gt; findAll()



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    try {
      List<TemplateV2> result = apiInstance.findAll();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#findAll");
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

[**List&lt;TemplateV2&gt;**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find all templates |  -  |

<a id="findByContext"></a>
# **findByContext**
> List&lt;TemplateV2&gt; findByContext(context)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    Context context = Context.fromValue("INVOICE"); // Context | 
    try {
      List<TemplateV2> result = apiInstance.findByContext(context);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#findByContext");
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
| **context** | [**Context**](.md)|  | [enum: INVOICE, PEPPOL, C_V] |

### Return type

[**List&lt;TemplateV2&gt;**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find templates by context |  -  |

<a id="findByIds"></a>
# **findByIds**
> List&lt;TemplateV2&gt; findByIds(ids)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    List<String> ids = Arrays.asList(); // List<String> | 
    try {
      List<TemplateV2> result = apiInstance.findByIds(ids);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#findByIds");
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
| **ids** | [**List&lt;String&gt;**](String.md)|  | |

### Return type

[**List&lt;TemplateV2&gt;**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find By ids |  -  |

<a id="findByType"></a>
# **findByType**
> List&lt;TemplateV2&gt; findByType(templateType)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    TemplateType templateType = TemplateType.fromValue("HTML"); // TemplateType | 
    try {
      List<TemplateV2> result = apiInstance.findByType(templateType);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#findByType");
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
| **templateType** | [**TemplateType**](.md)|  | [enum: HTML, XML] |

### Return type

[**List&lt;TemplateV2&gt;**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find templates by type |  -  |

<a id="findOne"></a>
# **findOne**
> TemplateV2 findOne(templId)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    String templId = "templId_example"; // String | 
    try {
      TemplateV2 result = apiInstance.findOne(templId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#findOne");
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
| **templId** | **String**|  | |

### Return type

[**TemplateV2**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Find a template by id |  -  |

<a id="render"></a>
# **render**
> File render(renderRequest)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    RenderRequest renderRequest = new RenderRequest(); // RenderRequest | 
    try {
      File result = apiInstance.render(renderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#render");
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
| **renderRequest** | [**RenderRequest**](RenderRequest.md)|  | |

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
| **200** | Render template |  -  |

<a id="upsert"></a>
# **upsert**
> TemplateV2 upsert(title, templateType, templateContext, files, id, description)



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.TemplateRoutesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    TemplateRoutesApi apiInstance = new TemplateRoutesApi(defaultClient);
    String title = "title_example"; // String | 
    TemplateType templateType = TemplateType.fromValue("HTML"); // TemplateType | 
    Context templateContext = Context.fromValue("INVOICE"); // Context | 
    List<File> files = Arrays.asList(); // List<File> | 
    String id = "id_example"; // String | 
    String description = "description_example"; // String | 
    try {
      TemplateV2 result = apiInstance.upsert(title, templateType, templateContext, files, id, description);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateRoutesApi#upsert");
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
| **title** | **String**|  | |
| **templateType** | [**TemplateType**](.md)|  | [enum: HTML, XML] |
| **templateContext** | [**Context**](.md)|  | [enum: INVOICE, PEPPOL, C_V] |
| **files** | **List&lt;File&gt;**|  | |
| **id** | **String**|  | [optional] |
| **description** | **String**|  | [optional] |

### Return type

[**TemplateV2**](TemplateV2.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upsert a template |  -  |

