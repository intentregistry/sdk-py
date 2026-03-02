# AuthLogoutRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**refresh_token** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.auth_logout_request import AuthLogoutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AuthLogoutRequest from a JSON string
auth_logout_request_instance = AuthLogoutRequest.from_json(json)
# print the JSON string representation of the object
print(AuthLogoutRequest.to_json())

# convert the object into a dict
auth_logout_request_dict = auth_logout_request_instance.to_dict()
# create an instance of AuthLogoutRequest from a dict
auth_logout_request_from_dict = AuthLogoutRequest.from_dict(auth_logout_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


