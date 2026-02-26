# AuthTokens


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | **str** |  | 
**refresh_token** | **str** |  | 
**expires_in** | **int** | Seconds until expiration | 

## Example

```python
from openapi_client.models.auth_tokens import AuthTokens

# TODO update the JSON string below
json = "{}"
# create an instance of AuthTokens from a JSON string
auth_tokens_instance = AuthTokens.from_json(json)
# print the JSON string representation of the object
print(AuthTokens.to_json())

# convert the object into a dict
auth_tokens_dict = auth_tokens_instance.to_dict()
# create an instance of AuthTokens from a dict
auth_tokens_from_dict = AuthTokens.from_dict(auth_tokens_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


