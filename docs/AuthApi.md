# openapi_client.AuthApi

All URIs are relative to *http://localhost:3001*

Method | HTTP request | Description
------------- | ------------- | -------------
[**auth_login**](AuthApi.md#auth_login) | **POST** /v1/auth/login | Login with email and password


# **auth_login**
> AuthTokens auth_login(login_request)

Login with email and password

### Example


```python
import openapi_client
from openapi_client.models.auth_tokens import AuthTokens
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

[**AuthTokens**](AuthTokens.md)

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

