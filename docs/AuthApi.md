# openapi_client.AuthApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auth_login**](AuthApi.md#auth_login) | **POST** /v1/auth/login | Login with email and password
[**auth_logout**](AuthApi.md#auth_logout) | **POST** /v1/auth/logout | Logout and revoke refresh sessions
[**auth_password_reset_confirm**](AuthApi.md#auth_password_reset_confirm) | **POST** /v1/auth/password/reset/confirm | Confirm password reset
[**auth_password_reset_request**](AuthApi.md#auth_password_reset_request) | **POST** /v1/auth/password/reset/request | Request password reset
[**auth_refresh**](AuthApi.md#auth_refresh) | **POST** /v1/auth/refresh | Refresh access token
[**auth_signup**](AuthApi.md#auth_signup) | **POST** /v1/auth/signup | Create account and start session
[**create_pat**](AuthApi.md#create_pat) | **POST** /v1/auth/tokens | Create PAT
[**delete_pat**](AuthApi.md#delete_pat) | **DELETE** /v1/auth/tokens/{id} | Delete PAT
[**list_pats**](AuthApi.md#list_pats) | **GET** /v1/auth/tokens | List personal access tokens (PAT)


# **auth_login**
> AuthSessionResponse auth_login(login_request)

Login with email and password

### Example


```python
import openapi_client
from openapi_client.models.auth_session_response import AuthSessionResponse
from openapi_client.models.login_request import LoginRequest
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
    api_instance = openapi_client.AuthApi(api_client)
    login_request = openapi_client.LoginRequest() # LoginRequest | 

    try:
        # Login with email and password
        api_response = api_instance.auth_login(login_request)
        print("The response of AuthApi->auth_login:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->auth_login: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_request** | [**LoginRequest**](LoginRequest.md)|  | 

### Return type

[**AuthSessionResponse**](AuthSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Login successful |  -  |
**401** | Invalid credentials |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auth_logout**
> auth_logout(auth_logout_request=auth_logout_request)

Logout and revoke refresh sessions

### Example

* Bearer (JWT-or-PAT) Authentication (bearerAuth):

```python
import openapi_client
from openapi_client.models.auth_logout_request import AuthLogoutRequest
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
    api_instance = openapi_client.AuthApi(api_client)
    auth_logout_request = openapi_client.AuthLogoutRequest() # AuthLogoutRequest |  (optional)

    try:
        # Logout and revoke refresh sessions
        api_instance.auth_logout(auth_logout_request=auth_logout_request)
    except Exception as e:
        print("Exception when calling AuthApi->auth_logout: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_logout_request** | [**AuthLogoutRequest**](AuthLogoutRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logout complete |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auth_password_reset_confirm**
> auth_password_reset_confirm(auth_password_reset_confirm_request)

Confirm password reset

### Example


```python
import openapi_client
from openapi_client.models.auth_password_reset_confirm_request import AuthPasswordResetConfirmRequest
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
    api_instance = openapi_client.AuthApi(api_client)
    auth_password_reset_confirm_request = openapi_client.AuthPasswordResetConfirmRequest() # AuthPasswordResetConfirmRequest | 

    try:
        # Confirm password reset
        api_instance.auth_password_reset_confirm(auth_password_reset_confirm_request)
    except Exception as e:
        print("Exception when calling AuthApi->auth_password_reset_confirm: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_password_reset_confirm_request** | [**AuthPasswordResetConfirmRequest**](AuthPasswordResetConfirmRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password changed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auth_password_reset_request**
> AuthPasswordResetRequest200Response auth_password_reset_request(auth_password_reset_request_request)

Request password reset

### Example


```python
import openapi_client
from openapi_client.models.auth_password_reset_request200_response import AuthPasswordResetRequest200Response
from openapi_client.models.auth_password_reset_request_request import AuthPasswordResetRequestRequest
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
    api_instance = openapi_client.AuthApi(api_client)
    auth_password_reset_request_request = openapi_client.AuthPasswordResetRequestRequest() # AuthPasswordResetRequestRequest | 

    try:
        # Request password reset
        api_response = api_instance.auth_password_reset_request(auth_password_reset_request_request)
        print("The response of AuthApi->auth_password_reset_request:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->auth_password_reset_request: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_password_reset_request_request** | [**AuthPasswordResetRequestRequest**](AuthPasswordResetRequestRequest.md)|  | 

### Return type

[**AuthPasswordResetRequest200Response**](AuthPasswordResetRequest200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Request accepted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auth_refresh**
> AuthSessionResponse auth_refresh(auth_refresh_request)

Refresh access token

### Example


```python
import openapi_client
from openapi_client.models.auth_refresh_request import AuthRefreshRequest
from openapi_client.models.auth_session_response import AuthSessionResponse
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
    api_instance = openapi_client.AuthApi(api_client)
    auth_refresh_request = openapi_client.AuthRefreshRequest() # AuthRefreshRequest | 

    try:
        # Refresh access token
        api_response = api_instance.auth_refresh(auth_refresh_request)
        print("The response of AuthApi->auth_refresh:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->auth_refresh: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_refresh_request** | [**AuthRefreshRequest**](AuthRefreshRequest.md)|  | 

### Return type

[**AuthSessionResponse**](AuthSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Refresh successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **auth_signup**
> AuthSessionResponse auth_signup(signup_request)

Create account and start session

### Example


```python
import openapi_client
from openapi_client.models.auth_session_response import AuthSessionResponse
from openapi_client.models.signup_request import SignupRequest
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
    api_instance = openapi_client.AuthApi(api_client)
    signup_request = openapi_client.SignupRequest() # SignupRequest | 

    try:
        # Create account and start session
        api_response = api_instance.auth_signup(signup_request)
        print("The response of AuthApi->auth_signup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->auth_signup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signup_request** | [**SignupRequest**](SignupRequest.md)|  | 

### Return type

[**AuthSessionResponse**](AuthSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Account created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_pat**
> create_pat()

Create PAT

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
    api_instance = openapi_client.AuthApi(api_client)

    try:
        # Create PAT
        api_instance.create_pat()
    except Exception as e:
        print("Exception when calling AuthApi->create_pat: %s\n" % e)
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
**201** | Token created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_pat**
> delete_pat(id)

Delete PAT

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
    api_instance = openapi_client.AuthApi(api_client)
    id = 56 # int | 

    try:
        # Delete PAT
        api_instance.delete_pat(id)
    except Exception as e:
        print("Exception when calling AuthApi->delete_pat: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | 

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
**200** | Token deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_pats**
> list_pats()

List personal access tokens (PAT)

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
    api_instance = openapi_client.AuthApi(api_client)

    try:
        # List personal access tokens (PAT)
        api_instance.list_pats()
    except Exception as e:
        print("Exception when calling AuthApi->list_pats: %s\n" % e)
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
**200** | Token list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

