# openapi_client.TrustedPublishingApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_packages_scope_name_versions_version_provenance_get**](TrustedPublishingApi.md#v1_packages_scope_name_versions_version_provenance_get) | **GET** /v1/packages/{scope}/{name}/versions/{version}/provenance | Get provenance for a package version
[**v1_packages_scope_name_versions_version_provenance_put**](TrustedPublishingApi.md#v1_packages_scope_name_versions_version_provenance_put) | **PUT** /v1/packages/{scope}/{name}/versions/{version}/provenance | Upsert provenance for a package version
[**v1_publish_oidc_exchange_post**](TrustedPublishingApi.md#v1_publish_oidc_exchange_post) | **POST** /v1/publish/oidc/exchange | Exchange trusted OIDC identity for short-lived publish token


# **v1_packages_scope_name_versions_version_provenance_get**
> v1_packages_scope_name_versions_version_provenance_get(scope, name, version)

Get provenance for a package version

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
    api_instance = openapi_client.TrustedPublishingApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str | 

    try:
        # Get provenance for a package version
        api_instance.v1_packages_scope_name_versions_version_provenance_get(scope, name, version)
    except Exception as e:
        print("Exception when calling TrustedPublishingApi->v1_packages_scope_name_versions_version_provenance_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**|  | 
 **name** | **str**|  | 
 **version** | **str**|  | 

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
**200** | Provenance record |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_packages_scope_name_versions_version_provenance_put**
> v1_packages_scope_name_versions_version_provenance_put(scope, name, version)

Upsert provenance for a package version

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
    api_instance = openapi_client.TrustedPublishingApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str | 

    try:
        # Upsert provenance for a package version
        api_instance.v1_packages_scope_name_versions_version_provenance_put(scope, name, version)
    except Exception as e:
        print("Exception when calling TrustedPublishingApi->v1_packages_scope_name_versions_version_provenance_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**|  | 
 **name** | **str**|  | 
 **version** | **str**|  | 

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
**200** | Provenance updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_publish_oidc_exchange_post**
> v1_publish_oidc_exchange_post()

Exchange trusted OIDC identity for short-lived publish token

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
    api_instance = openapi_client.TrustedPublishingApi(api_client)

    try:
        # Exchange trusted OIDC identity for short-lived publish token
        api_instance.v1_publish_oidc_exchange_post()
    except Exception as e:
        print("Exception when calling TrustedPublishingApi->v1_publish_oidc_exchange_post: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**201** | Exchange successful |  -  |
**409** | Replay detected for active trusted publish session |  -  |
**403** | Trust policy validation failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

