# openapi_client.RegistryIndexApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_index_changes_get**](RegistryIndexApi.md#v1_index_changes_get) | **GET** /v1/index/changes | Incremental index change feed
[**v1_index_pkg_scope_name_get**](RegistryIndexApi.md#v1_index_pkg_scope_name_get) | **GET** /v1/index/pkg/{scope}/{name} | Compact package metadata for clients


# **v1_index_changes_get**
> v1_index_changes_get(since=since)

Incremental index change feed

### Example


```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:3001
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost:3001"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.RegistryIndexApi(api_client)
    since = 56 # int |  (optional)

    try:
        # Incremental index change feed
        api_instance.v1_index_changes_get(since=since)
    except Exception as e:
        print("Exception when calling RegistryIndexApi->v1_index_changes_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **since** | **int**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Changes feed |  -  |
**304** | Not modified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_index_pkg_scope_name_get**
> v1_index_pkg_scope_name_get(scope, name)

Compact package metadata for clients

### Example


```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:3001
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost:3001"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.RegistryIndexApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 

    try:
        # Compact package metadata for clients
        api_instance.v1_index_pkg_scope_name_get(scope, name)
    except Exception as e:
        print("Exception when calling RegistryIndexApi->v1_index_pkg_scope_name_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**|  | 
 **name** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Index package document |  -  |
**304** | Not modified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

