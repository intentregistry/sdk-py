# openapi_client.PackagesApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_package**](PackagesApi.md#create_package) | **POST** /v1/packages | Create package
[**list_packages**](PackagesApi.md#list_packages) | **GET** /v1/packages | List public packages for catalog discovery
[**resolve_package**](PackagesApi.md#resolve_package) | **GET** /v1/packages/{scope}/{name}/resolve | Resolve package install target


# **create_package**
> create_package()

Create package

### Example

* Bearer (JWT-or-PAT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost:3001
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost:3001"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT-or-PAT): bearerAuth
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.PackagesApi(api_client)

    try:
        # Create package
        api_instance.create_package()
    except Exception as e:
        print("Exception when calling PackagesApi->create_package: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Package created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_packages**
> PackagesListResponse list_packages(q=q, limit=limit, offset=offset)

List public packages for catalog discovery

### Example


```python
import openapi_client
from openapi_client.models.packages_list_response import PackagesListResponse
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
    q = 'q_example' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List public packages for catalog discovery
        api_response = api_instance.list_packages(q=q, limit=limit, offset=offset)
        print("The response of PackagesApi->list_packages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PackagesApi->list_packages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**PackagesListResponse**](PackagesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Public package list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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

