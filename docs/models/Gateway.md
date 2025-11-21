# Gateway

An API gateway consists of the generic rules and configurations of an API Gateway. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**logs** | **bool** | This field enables or disables the collection and reporting of logs for observability of this instance. | [optional] [default to False]
**metrics** | **bool** | This field enables or disables the collection and reporting of metrics for observability of this instance. | [optional] [default to False]
**custom_domains** | [**list[GatewayCustomDomainsInner]**](GatewayCustomDomainsInner.md) |  | [optional] 

## Example

```python
from ionoscloud_api_gateway.models.gateway import Gateway

# TODO update the JSON string below
json = "{}"
# create an instance of Gateway from a JSON string
gateway_instance = Gateway.from_json(json)
# print the JSON string representation of the object
print(Gateway.to_json())

# convert the object into a dict
gateway_dict = gateway_instance.to_dict()
# create an instance of Gateway from a dict
gateway_from_dict = Gateway.from_dict(gateway_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


