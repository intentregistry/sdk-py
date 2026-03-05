# PackagesPagination


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**limit** | **int** |  | 
**offset** | **int** |  | 

## Example

```python
from openapi_client.models.packages_pagination import PackagesPagination

# TODO update the JSON string below
json = "{}"
# create an instance of PackagesPagination from a JSON string
packages_pagination_instance = PackagesPagination.from_json(json)
# print the JSON string representation of the object
print(PackagesPagination.to_json())

# convert the object into a dict
packages_pagination_dict = packages_pagination_instance.to_dict()
# create an instance of PackagesPagination from a dict
packages_pagination_from_dict = PackagesPagination.from_dict(packages_pagination_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


