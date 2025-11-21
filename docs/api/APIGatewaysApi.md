# ionoscloud_api_gateway.APIGatewaysApi

All URIs are relative to *https://apigateway.de-txl.ionos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apigateways_delete**](APIGatewaysApi.md#apigateways_delete) | **DELETE** /gateways/{apigatewayId} | Delete Gateway
[**apigateways_find_by_id**](APIGatewaysApi.md#apigateways_find_by_id) | **GET** /gateways/{apigatewayId} | Retrieve Gateway
[**apigateways_get**](APIGatewaysApi.md#apigateways_get) | **GET** /gateways | Retrieve all Apigateways
[**apigateways_post**](APIGatewaysApi.md#apigateways_post) | **POST** /gateways | Create Gateway
[**apigateways_put**](APIGatewaysApi.md#apigateways_put) | **PUT** /gateways/{apigatewayId} | Ensure Gateway


# **apigateways_delete**
> apigateways_delete(apigateway_id)

Delete Gateway

Deletes the specified Gateway.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://apigateway.de-txl.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_api_gateway.Configuration(
    host = "https://apigateway.de-txl.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_api_gateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_api_gateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_api_gateway.APIGatewaysApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.

    try:
        # Delete Gateway
        api_instance.apigateways_delete(apigateway_id)
    except Exception as e:
        print("Exception when calling APIGatewaysApi->apigateways_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 

### Return type

void (empty response body)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Deleting Gateway was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_find_by_id**
> GatewayRead apigateways_find_by_id(apigateway_id)

Retrieve Gateway

Returns the Gateway by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.gateway_read import GatewayRead
from ionoscloud_api_gateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://apigateway.de-txl.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_api_gateway.Configuration(
    host = "https://apigateway.de-txl.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_api_gateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_api_gateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_api_gateway.APIGatewaysApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.

    try:
        # Retrieve Gateway
        api_response = api_instance.apigateways_find_by_id(apigateway_id)
        print("The response of APIGatewaysApi->apigateways_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIGatewaysApi->apigateways_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 

### Return type

[**GatewayRead**](GatewayRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting Gateway was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_get**
> GatewayReadList apigateways_get(offset=offset, limit=limit, order_by=order_by)

Retrieve all Apigateways

This endpoint enables retrieving all Apigateways using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.gateway_read_list import GatewayReadList
from ionoscloud_api_gateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://apigateway.de-txl.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_api_gateway.Configuration(
    host = "https://apigateway.de-txl.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_api_gateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_api_gateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_api_gateway.APIGatewaysApi(api_client)
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use together with limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use together with offset for pagination. (optional) (default to 100)
    order_by = -createdDate # str | The field to order the results by. If not provided, the results will be ordered by the default field. (optional) (default to -createdDate)

    try:
        # Retrieve all Apigateways
        api_response = api_instance.apigateways_get(offset=offset, limit=limit, order_by=order_by)
        print("The response of APIGatewaysApi->apigateways_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIGatewaysApi->apigateways_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use together with limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use together with offset for pagination. | [optional] [default to 100]
 **order_by** | **str**| The field to order the results by. If not provided, the results will be ordered by the default field. | [optional] [default to -createdDate]

### Return type

[**GatewayReadList**](GatewayReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Gateways successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_post**
> GatewayRead apigateways_post(gateway_create)

Create Gateway

Creates a new Gateway.

The full Gateway needs to be provided to create the object.
Optional data will be filled with defaults or left empty.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.gateway_create import GatewayCreate
from ionoscloud_api_gateway.models.gateway_read import GatewayRead
from ionoscloud_api_gateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://apigateway.de-txl.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_api_gateway.Configuration(
    host = "https://apigateway.de-txl.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_api_gateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_api_gateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_api_gateway.APIGatewaysApi(api_client)
    gateway_create = ionoscloud_api_gateway.GatewayCreate() # GatewayCreate | Gateway to create.

    try:
        # Create Gateway
        api_response = api_instance.apigateways_post(gateway_create)
        print("The response of APIGatewaysApi->apigateways_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIGatewaysApi->apigateways_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gateway_create** | [**GatewayCreate**](GatewayCreate.md)| Gateway to create. | 

### Return type

[**GatewayRead**](GatewayRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Gateway successfully created. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_put**
> GatewayRead apigateways_put(apigateway_id, gateway_ensure)

Ensure Gateway

Ensures that the Gateway with the provided ID is created or modified.
The full Gateway needs to be provided to ensure
(either update or create) the Gateway. Non present data will
only be filled with defaults or left empty, but not take
previous values into consideration.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.gateway_ensure import GatewayEnsure
from ionoscloud_api_gateway.models.gateway_read import GatewayRead
from ionoscloud_api_gateway.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://apigateway.de-txl.ionos.com
# See configuration.py for a list of all supported configuration parameters.
configuration = ionoscloud_api_gateway.Configuration(
    host = "https://apigateway.de-txl.ionos.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): tokenAuth
configuration = ionoscloud_api_gateway.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ionoscloud_api_gateway.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ionoscloud_api_gateway.APIGatewaysApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    gateway_ensure = ionoscloud_api_gateway.GatewayEnsure() # GatewayEnsure | update Gateway

    try:
        # Ensure Gateway
        api_response = api_instance.apigateways_put(apigateway_id, gateway_ensure)
        print("The response of APIGatewaysApi->apigateways_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling APIGatewaysApi->apigateways_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **gateway_ensure** | [**GatewayEnsure**](GatewayEnsure.md)| update Gateway | 

### Return type

[**GatewayRead**](GatewayRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Gateway successfully updated. |  -  |
**201** | Gateway successfully ensured. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**409** | ### Conflict The UUID is already taken by another party, follow the guides to generate UUIDs uniquely.  |  -  |
**415** | ### Unsupported Media Type The request has an unsupported media type.  |  -  |
**422** | ### Unprocessable Entity The request was well-formed but was unable to be followed due to semantic errors.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

