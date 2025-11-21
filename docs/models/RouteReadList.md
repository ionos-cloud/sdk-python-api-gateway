# RouteReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | The offset specified in the request (if none was specified, the default offset is 0).  | [readonly] 
**limit** | **int** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  | [readonly] 
**links** | [**Links**](Links.md) |  | 
**id** | **str** | ID of the Route. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Route. | 
**items** | [**list[RouteRead]**](RouteRead.md) | The list of Route resources. | [optional] 

## Example

```python
from ionoscloud_api_gateway.models.route_read_list import RouteReadList

# TODO update the JSON string below
json = "{}"
# create an instance of RouteReadList from a JSON string
route_read_list_instance = RouteReadList.from_json(json)
# print the JSON string representation of the object
print(RouteReadList.to_json())

# convert the object into a dict
route_read_list_dict = route_read_list_instance.to_dict()
# create an instance of RouteReadList from a dict
route_read_list_from_dict = RouteReadList.from_dict(route_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


