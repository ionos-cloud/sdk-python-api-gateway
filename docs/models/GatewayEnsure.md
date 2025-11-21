# GatewayEnsure


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Gateway. | 
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Gateway**](Gateway.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.gateway_ensure import GatewayEnsure

# TODO update the JSON string below
json = "{}"
# create an instance of GatewayEnsure from a JSON string
gateway_ensure_instance = GatewayEnsure.from_json(json)
# print the JSON string representation of the object
print(GatewayEnsure.to_json())

# convert the object into a dict
gateway_ensure_dict = gateway_ensure_instance.to_dict()
# create an instance of GatewayEnsure from a dict
gateway_ensure_from_dict = GatewayEnsure.from_dict(gateway_ensure_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


