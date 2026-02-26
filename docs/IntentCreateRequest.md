# IntentCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**title** | **str** |  | 
**description** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.intent_create_request import IntentCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IntentCreateRequest from a JSON string
intent_create_request_instance = IntentCreateRequest.from_json(json)
# print the JSON string representation of the object
print(IntentCreateRequest.to_json())

# convert the object into a dict
intent_create_request_dict = intent_create_request_instance.to_dict()
# create an instance of IntentCreateRequest from a dict
intent_create_request_from_dict = IntentCreateRequest.from_dict(intent_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


