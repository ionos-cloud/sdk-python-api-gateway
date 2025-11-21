# GatewayCreate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metadata** | **dict[str, object]** | Metadata | [optional] 
**properties** | [**Gateway**](Gateway.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.gateway_create import GatewayCreate

# TODO update the JSON string below
json = "{}"
# create an instance of GatewayCreate from a JSON string
gateway_create_instance = GatewayCreate.from_json(json)
# print the JSON string representation of the object
print(GatewayCreate.to_json())

# convert the object into a dict
gateway_create_dict = gateway_create_instance.to_dict()
# create an instance of GatewayCreate from a dict
gateway_create_from_dict = GatewayCreate.from_dict(gateway_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


