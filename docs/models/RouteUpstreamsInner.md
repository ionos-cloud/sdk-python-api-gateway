# RouteUpstreamsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scheme** | **str** | The target URL of the upstream. | [default to 'http']
**loadbalancer** | **str** | The load balancer algorithm. | [default to 'roundrobin']
**host** | **str** | The host of the upstream. | 
**port** | **int** | The port of the upstream. | [default to 80]
**weight** | **int** | Weight with which to split traffic to the upstream. | [optional] [default to 100]

## Example

```python
from ionoscloud_api_gateway.models.route_upstreams_inner import RouteUpstreamsInner

# TODO update the JSON string below
json = "{}"
# create an instance of RouteUpstreamsInner from a JSON string
route_upstreams_inner_instance = RouteUpstreamsInner.from_json(json)
# print the JSON string representation of the object
print(RouteUpstreamsInner.to_json())

# convert the object into a dict
route_upstreams_inner_dict = route_upstreams_inner_instance.to_dict()
# create an instance of RouteUpstreamsInner from a dict
route_upstreams_inner_from_dict = RouteUpstreamsInner.from_dict(route_upstreams_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


