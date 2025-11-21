# MetadataWithEndpoint


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_date** | **datetime** | The ISO 8601 creation timestamp. | [optional] [readonly] 
**created_by** | **str** | Unique name of the identity that created the resource. | [optional] [readonly] 
**created_by_user_id** | **str** | Unique id of the identity that created the resource. | [optional] [readonly] 
**last_modified_date** | **datetime** | The ISO 8601 modified timestamp. | [optional] [readonly] 
**last_modified_by** | **str** | Unique name of the identity that last modified the resource. | [optional] [readonly] 
**last_modified_by_user_id** | **str** | Unique id of the identity that last modified the resource. | [optional] [readonly] 
**resource_urn** | **str** | Unique name of the resource. | [optional] [readonly] 
**status** | **str** | The status of the object. The status can be: * &#x60;AVAILABLE&#x60; - resource exists and is healthy. * &#x60;PROVISIONING&#x60; - resource is being created or updated. * &#x60;DESTROYING&#x60; - delete command was issued, the resource is being deleted. * &#x60;FAILED&#x60; - resource failed, details in &#x60;failureMessage&#x60;.  | [readonly] 
**status_message** | **str** | The message of the failure if the status is &#x60;FAILED&#x60;.  | [optional] [readonly] 
**public_endpoint** | **str** | The public endpoint of the API Gateway instance.  | [readonly] 

## Example

```python
from ionoscloud_api_gateway.models.metadata_with_endpoint import MetadataWithEndpoint

# TODO update the JSON string below
json = "{}"
# create an instance of MetadataWithEndpoint from a JSON string
metadata_with_endpoint_instance = MetadataWithEndpoint.from_json(json)
# print the JSON string representation of the object
print(MetadataWithEndpoint.to_json())

# convert the object into a dict
metadata_with_endpoint_dict = metadata_with_endpoint_instance.to_dict()
# create an instance of MetadataWithEndpoint from a dict
metadata_with_endpoint_from_dict = MetadataWithEndpoint.from_dict(metadata_with_endpoint_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


