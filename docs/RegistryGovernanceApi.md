# openapi_client.RegistryGovernanceApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1_packages_scope_name_tags_get**](RegistryGovernanceApi.md#v1_packages_scope_name_tags_get) | **GET** /v1/packages/{scope}/{name}/tags | List dist-tags for a package
[**v1_packages_scope_name_tags_tag_put**](RegistryGovernanceApi.md#v1_packages_scope_name_tags_tag_put) | **PUT** /v1/packages/{scope}/{name}/tags/{tag} | Set dist-tag target version (admin)
[**v1_packages_scope_name_versions_version_deprecate_put**](RegistryGovernanceApi.md#v1_packages_scope_name_versions_version_deprecate_put) | **PUT** /v1/packages/{scope}/{name}/versions/{version}/deprecate | Deprecate or clear deprecation for a version
[**v1_packages_scope_name_versions_version_quarantine_put**](RegistryGovernanceApi.md#v1_packages_scope_name_versions_version_quarantine_put) | **PUT** /v1/packages/{scope}/{name}/versions/{version}/quarantine | Quarantine a version (admin)
[**v1_packages_scope_name_versions_version_unquarantine_put**](RegistryGovernanceApi.md#v1_packages_scope_name_versions_version_unquarantine_put) | **PUT** /v1/packages/{scope}/{name}/versions/{version}/unquarantine | Remove quarantine from a version (admin)


# **v1_packages_scope_name_tags_get**
> v1_packages_scope_name_tags_get(scope, name)

List dist-tags for a package

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
    api_instance = openapi_client.RegistryGovernanceApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 

    try:
        # List dist-tags for a package
        api_instance.v1_packages_scope_name_tags_get(scope, name)
    except Exception as e:
        print("Exception when calling RegistryGovernanceApi->v1_packages_scope_name_tags_get: %s\n" % e)
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
**200** | Dist-tags map |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_packages_scope_name_tags_tag_put**
> v1_packages_scope_name_tags_tag_put(scope, name, tag)

Set dist-tag target version (admin)

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
    api_instance = openapi_client.RegistryGovernanceApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    tag = 'tag_example' # str | 

    try:
        # Set dist-tag target version (admin)
        api_instance.v1_packages_scope_name_tags_tag_put(scope, name, tag)
    except Exception as e:
        print("Exception when calling RegistryGovernanceApi->v1_packages_scope_name_tags_tag_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **str**|  | 
 **name** | **str**|  | 
 **tag** | **str**|  | 

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
**200** | Tag updated |  -  |
**429** | Governance mutation cooldown/rate cap exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_packages_scope_name_versions_version_deprecate_put**
> v1_packages_scope_name_versions_version_deprecate_put(scope, name, version)

Deprecate or clear deprecation for a version

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
    api_instance = openapi_client.RegistryGovernanceApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str | 

    try:
        # Deprecate or clear deprecation for a version
        api_instance.v1_packages_scope_name_versions_version_deprecate_put(scope, name, version)
    except Exception as e:
        print("Exception when calling RegistryGovernanceApi->v1_packages_scope_name_versions_version_deprecate_put: %s\n" % e)
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
**200** | Deprecation updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_packages_scope_name_versions_version_quarantine_put**
> v1_packages_scope_name_versions_version_quarantine_put(scope, name, version)

Quarantine a version (admin)

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
    api_instance = openapi_client.RegistryGovernanceApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str | 

    try:
        # Quarantine a version (admin)
        api_instance.v1_packages_scope_name_versions_version_quarantine_put(scope, name, version)
    except Exception as e:
        print("Exception when calling RegistryGovernanceApi->v1_packages_scope_name_versions_version_quarantine_put: %s\n" % e)
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
**200** | Version quarantined |  -  |
**429** | Governance mutation cooldown/rate cap exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **v1_packages_scope_name_versions_version_unquarantine_put**
> v1_packages_scope_name_versions_version_unquarantine_put(scope, name, version)

Remove quarantine from a version (admin)

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
    api_instance = openapi_client.RegistryGovernanceApi(api_client)
    scope = 'scope_example' # str | 
    name = 'name_example' # str | 
    version = 'version_example' # str | 

    try:
        # Remove quarantine from a version (admin)
        api_instance.v1_packages_scope_name_versions_version_unquarantine_put(scope, name, version)
    except Exception as e:
        print("Exception when calling RegistryGovernanceApi->v1_packages_scope_name_versions_version_unquarantine_put: %s\n" % e)
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
**200** | Version unquarantined |  -  |
**429** | Governance mutation cooldown/rate cap exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

