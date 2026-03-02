# AuthPasswordResetRequestRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 

## Example

```python
from openapi_client.models.auth_password_reset_request_request import AuthPasswordResetRequestRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AuthPasswordResetRequestRequest from a JSON string
auth_password_reset_request_request_instance = AuthPasswordResetRequestRequest.from_json(json)
# print the JSON string representation of the object
print(AuthPasswordResetRequestRequest.to_json())

# convert the object into a dict
auth_password_reset_request_request_dict = auth_password_reset_request_request_instance.to_dict()
# create an instance of AuthPasswordResetRequestRequest from a dict
auth_password_reset_request_request_from_dict = AuthPasswordResetRequestRequest.from_dict(auth_password_reset_request_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


