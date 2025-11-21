# GatewayRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The ID (UUID) of the Gateway. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Gateway. | 
**metadata** | [**MetadataWithEndpoint**](MetadataWithEndpoint.md) |  | 
**properties** | [**Gateway**](Gateway.md) |  | 

## Example

```python
from ionoscloud_api_gateway.models.gateway_read import GatewayRead

# TODO update the JSON string below
json = "{}"
# create an instance of GatewayRead from a JSON string
gateway_read_instance = GatewayRead.from_json(json)
# print the JSON string representation of the object
print(GatewayRead.to_json())

# convert the object into a dict
gateway_read_dict = gateway_read_instance.to_dict()
# create an instance of GatewayRead from a dict
gateway_read_from_dict = GatewayRead.from_dict(gateway_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


