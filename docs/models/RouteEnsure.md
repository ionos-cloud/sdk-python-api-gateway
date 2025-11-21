# RouteEnsure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Route. | 
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Route**](Route.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.route_ensure import RouteEnsure

# TODO update the JSON string below
json = "{}"
# create an instance of RouteEnsure from a JSON string
route_ensure_instance = RouteEnsure.from_json(json)
# print the JSON string representation of the object
print(RouteEnsure.to_json())

# convert the object into a dict
route_ensure_dict = route_ensure_instance.to_dict()
# create an instance of RouteEnsure from a dict
route_ensure_from_dict = RouteEnsure.from_dict(route_ensure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


