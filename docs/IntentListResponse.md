# IntentListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Intent]**](Intent.md) |  | 
**next_cursor** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.intent_list_response import IntentListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IntentListResponse from a JSON string
intent_list_response_instance = IntentListResponse.from_json(json)
# print the JSON string representation of the object
print(IntentListResponse.to_json())

# convert the object into a dict
intent_list_response_dict = intent_list_response_instance.to_dict()
# create an instance of IntentListResponse from a dict
intent_list_response_from_dict = IntentListResponse.from_dict(intent_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


