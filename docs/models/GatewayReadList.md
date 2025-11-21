# GatewayReadList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offset** | **int** | The offset specified in the request (if none was specified, the default offset is 0).  | [readonly] 
**limit** | **int** | The limit specified in the request (if none was specified, use the endpoint&#39;s default pagination limit).  | [readonly] 
**links** | [**Links**](Links.md) |  | 
**id** | **str** | ID of the Gateway. | 
**type** | **str** | The type of the resource. | 
**href** | **str** | The URL of the Gateway. | 
**items** | [**list[GatewayRead]**](GatewayRead.md) | The list of Gateway resources. | [optional] 

## Example

```python
from ionoscloud_api_gateway.models.gateway_read_list import GatewayReadList

# TODO update the JSON string below
json = "{}"
# create an instance of GatewayReadList from a JSON string
gateway_read_list_instance = GatewayReadList.from_json(json)
# print the JSON string representation of the object
print(GatewayReadList.to_json())

# convert the object into a dict
gateway_read_list_dict = gateway_read_list_instance.to_dict()
# create an instance of GatewayReadList from a dict
gateway_read_list_from_dict = GatewayReadList.from_dict(gateway_read_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


