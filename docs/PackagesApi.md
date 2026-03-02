# openapi_client.PackagesApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**resolve_package**](PackagesApi.md#resolve_package) | **GET** /v1/packages/{scope}/{name}/resolve | Resolve package install target


# **resolve_package**
> resolve_package(scope, name, version=version, channel=channel)

Resolve package install target

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
    api_instance = openapi_client.PackagesApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str |  (optional)
    channel = 'channel_example' # str |  (optional)

    try:
        # Resolve package install target
        api_instance.resolve_package(scope, name, version=version, channel=channel)
    except Exception as e:
        print("Exception when calling PackagesApi->resolve_package: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**|  | 
 **name** | **str**|  | 
 **version** | **str**|  | [optional] 
 **channel** | **str**|  | [optional] 

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
**200** | Resolution result |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

