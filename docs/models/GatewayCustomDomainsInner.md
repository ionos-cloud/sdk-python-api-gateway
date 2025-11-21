# GatewayCustomDomainsInner

The custom domain that the API Gateway instance should listen on. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The domain name of the distribution. | [optional] 
**certificate_id** | **str** | The ID of the certificate to use for the distribution. | [optional] 

## Example

```python
from ionoscloud_api_gateway.models.gateway_custom_domains_inner import GatewayCustomDomainsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GatewayCustomDomainsInner from a JSON string
gateway_custom_domains_inner_instance = GatewayCustomDomainsInner.from_json(json)
# print the JSON string representation of the object
print(GatewayCustomDomainsInner.to_json())

# convert the object into a dict
gateway_custom_domains_inner_dict = gateway_custom_domains_inner_instance.to_dict()
# create an instance of GatewayCustomDomainsInner from a dict
gateway_custom_domains_inner_from_dict = GatewayCustomDomainsInner.from_dict(gateway_custom_domains_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


