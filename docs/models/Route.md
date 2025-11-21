# Route

A route is a rule that maps an incoming request to a specific backend service. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The name of the route. | 
**type** | **str** | This field specifies the protocol used by the ingress to route traffic to the backend service. | [default to 'http']
**paths** | **list[str]** | The paths that the route should match.  | 
**methods** | **list[str]** | The HTTP methods that the route should match.  | 
**websocket** | **bool** | To enable websocket support. | [optional] [default to False]
**upstreams** | [**list[RouteUpstreamsInner]**](RouteUpstreamsInner.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.route import Route

# TODO update the JSON string below
json = "{}"
# create an instance of Route from a JSON string
route_instance = Route.from_json(json)
# print the JSON string representation of the object
print(Route.to_json())

# convert the object into a dict
route_dict = route_instance.to_dict()
# create an instance of Route from a dict
route_from_dict = Route.from_dict(route_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


