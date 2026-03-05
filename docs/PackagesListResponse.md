# PackagesListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[PackageListItem]**](PackageListItem.md) |  | 
**pagination** | [**PackagesPagination**](PackagesPagination.md) |  | 

## Example

```python
from openapi_client.models.packages_list_response import PackagesListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PackagesListResponse from a JSON string
packages_list_response_instance = PackagesListResponse.from_json(json)
# print the JSON string representation of the object
print(PackagesListResponse.to_json())

# convert the object into a dict
packages_list_response_dict = packages_list_response_instance.to_dict()
# create an instance of PackagesListResponse from a dict
packages_list_response_from_dict = PackagesListResponse.from_dict(packages_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


