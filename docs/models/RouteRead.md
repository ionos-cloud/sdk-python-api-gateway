# RouteRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Route. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Route. | 
**metadata** | [**MetadataWithEndpoint**](MetadataWithEndpoint.md) |  | 
**properties** | [**Route**](Route.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.route_read import RouteRead

# TODO update the JSON string below
json = "{}"
# create an instance of RouteRead from a JSON string
route_read_instance = RouteRead.from_json(json)
# print the JSON string representation of the object
print(RouteRead.to_json())

# convert the object into a dict
route_read_dict = route_read_instance.to_dict()
# create an instance of RouteRead from a dict
route_read_from_dict = RouteRead.from_dict(route_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


