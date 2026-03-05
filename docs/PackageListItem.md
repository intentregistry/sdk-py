# PackageListItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**scope** | **str** |  | 
**name** | **str** |  | 
**visibility** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from openapi_client.models.package_list_item import PackageListItem

# TODO update the JSON string below
json = "{}"
# create an instance of PackageListItem from a JSON string
package_list_item_instance = PackageListItem.from_json(json)
# print the JSON string representation of the object
print(PackageListItem.to_json())

# convert the object into a dict
package_list_item_dict = package_list_item_instance.to_dict()
# create an instance of PackageListItem from a dict
package_list_item_from_dict = PackageListItem.from_dict(package_list_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


