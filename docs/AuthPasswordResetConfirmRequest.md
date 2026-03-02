# AuthPasswordResetConfirmRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | 
**new_password** | **str** |  | 

## Example

```python
from openapi_client.models.auth_password_reset_confirm_request import AuthPasswordResetConfirmRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AuthPasswordResetConfirmRequest from a JSON string
auth_password_reset_confirm_request_instance = AuthPasswordResetConfirmRequest.from_json(json)
# print the JSON string representation of the object
print(AuthPasswordResetConfirmRequest.to_json())

# convert the object into a dict
auth_password_reset_confirm_request_dict = auth_password_reset_confirm_request_instance.to_dict()
# create an instance of AuthPasswordResetConfirmRequest from a dict
auth_password_reset_confirm_request_from_dict = AuthPasswordResetConfirmRequest.from_dict(auth_password_reset_confirm_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


