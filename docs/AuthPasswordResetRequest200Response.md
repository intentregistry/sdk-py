# AuthPasswordResetRequest200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**reset_token** | **str** |  | [optional] 
**expires_in** | **int** |  | [optional] 

## Example

```python
from openapi_client.models.auth_password_reset_request200_response import AuthPasswordResetRequest200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AuthPasswordResetRequest200Response from a JSON string
auth_password_reset_request200_response_instance = AuthPasswordResetRequest200Response.from_json(json)
# print the JSON string representation of the object
print(AuthPasswordResetRequest200Response.to_json())

# convert the object into a dict
auth_password_reset_request200_response_dict = auth_password_reset_request200_response_instance.to_dict()
# create an instance of AuthPasswordResetRequest200Response from a dict
auth_password_reset_request200_response_from_dict = AuthPasswordResetRequest200Response.from_dict(auth_password_reset_request200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


