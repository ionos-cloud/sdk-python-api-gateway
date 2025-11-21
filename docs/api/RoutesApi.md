# ionoscloud_api_gateway.RoutesApi

All URIs are relative to *https://apigateway.de-txl.ionos.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apigateways_routes_delete**](RoutesApi.md#apigateways_routes_delete) | **DELETE** /gateways/{apigatewayId}/routes/{routeId} | Delete Route
[**apigateways_routes_find_by_id**](RoutesApi.md#apigateways_routes_find_by_id) | **GET** /gateways/{apigatewayId}/routes/{routeId} | Retrieve Route
[**apigateways_routes_get**](RoutesApi.md#apigateways_routes_get) | **GET** /gateways/{apigatewayId}/routes | Retrieve all Routes
[**apigateways_routes_post**](RoutesApi.md#apigateways_routes_post) | **POST** /gateways/{apigatewayId}/routes | Create Route
[**apigateways_routes_put**](RoutesApi.md#apigateways_routes_put) | **PUT** /gateways/{apigatewayId}/routes/{routeId} | Ensure Route


# **apigateways_routes_delete**
> apigateways_routes_delete(apigateway_id, route_id)

Delete Route

Deletes the specified Route.

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
    api_instance = ionoscloud_api_gateway.RoutesApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    route_id = '50982018-bb17-5cb9-bcd4-97f8bbc7dc23' # str | The ID (UUID) of the Route.

    try:
        # Delete Route
        api_instance.apigateways_routes_delete(apigateway_id, route_id)
    except Exception as e:
        print("Exception when calling RoutesApi->apigateways_routes_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **route_id** | **str**| The ID (UUID) of the Route. | 

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
**202** | Deleting Route was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_routes_find_by_id**
> RouteRead apigateways_routes_find_by_id(apigateway_id, route_id)

Retrieve Route

Returns the Route by ID.

### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.route_read import RouteRead
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
    api_instance = ionoscloud_api_gateway.RoutesApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    route_id = '50982018-bb17-5cb9-bcd4-97f8bbc7dc23' # str | The ID (UUID) of the Route.

    try:
        # Retrieve Route
        api_response = api_instance.apigateways_routes_find_by_id(apigateway_id, route_id)
        print("The response of RoutesApi->apigateways_routes_find_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutesApi->apigateways_routes_find_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **route_id** | **str**| The ID (UUID) of the Route. | 

### Return type

[**RouteRead**](RouteRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Getting Route was successful. |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**404** | ### Not Found The resource that was requested could not be found.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_routes_get**
> RouteReadList apigateways_routes_get(apigateway_id, offset=offset, limit=limit, order_by=order_by)

Retrieve all Routes

This endpoint enables retrieving all Routes using
pagination and optional filters.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.route_read_list import RouteReadList
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
    api_instance = ionoscloud_api_gateway.RoutesApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    offset = 0 # int | The first element (of the total list of elements) to include in the response. Use together with limit for pagination. (optional) (default to 0)
    limit = 100 # int | The maximum number of elements to return. Use together with offset for pagination. (optional) (default to 100)
    order_by = -createdDate # str | The field to order the results by. If not provided, the results will be ordered by the default field. (optional) (default to -createdDate)

    try:
        # Retrieve all Routes
        api_response = api_instance.apigateways_routes_get(apigateway_id, offset=offset, limit=limit, order_by=order_by)
        print("The response of RoutesApi->apigateways_routes_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutesApi->apigateways_routes_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **offset** | **int**| The first element (of the total list of elements) to include in the response. Use together with limit for pagination. | [optional] [default to 0]
 **limit** | **int**| The maximum number of elements to return. Use together with offset for pagination. | [optional] [default to 100]
 **order_by** | **str**| The field to order the results by. If not provided, the results will be ordered by the default field. | [optional] [default to -createdDate]

### Return type

[**RouteReadList**](RouteReadList.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Returned all requested Gateways/{apigatewayid}/routes successfully.  |  -  |
**400** | ### Bad Request The request send to the API was malformed.  |  -  |
**401** | ### Unauthorized The request is missing authorization information or the authorization information provided are expired.  |  -  |
**403** | ### Not Allowed The user issuing the request does not have the needed permissions.  |  -  |
**429** | ### Too Many Requests The user has sent too many requests in a given amount of time.  |  -  |
**500** | ### Internal Server Error An internal error occurred. We apologize for the inconvenience!  |  -  |
**503** | ### Service Unavailable The server is currently unable to handle the request due to a temporary overloading or maintenance of the server.  |  -  |
**0** | ### Unexpected Internal Server Error An unexpected internal error occurred. We apologize for the inconvenience!  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apigateways_routes_post**
> RouteRead apigateways_routes_post(apigateway_id, route_create)

Create Route

Creates a new Route.

The full Route needs to be provided to create the object.
Optional data will be filled with defaults or left empty.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.route_create import RouteCreate
from ionoscloud_api_gateway.models.route_read import RouteRead
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
    api_instance = ionoscloud_api_gateway.RoutesApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    route_create = ionoscloud_api_gateway.RouteCreate() # RouteCreate | Route to create.

    try:
        # Create Route
        api_response = api_instance.apigateways_routes_post(apigateway_id, route_create)
        print("The response of RoutesApi->apigateways_routes_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutesApi->apigateways_routes_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **route_create** | [**RouteCreate**](RouteCreate.md)| Route to create. | 

### Return type

[**RouteRead**](RouteRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Route successfully created. |  -  |
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

# **apigateways_routes_put**
> RouteRead apigateways_routes_put(apigateway_id, route_id, route_ensure)

Ensure Route

Ensures that the Route with the provided ID is created or modified.
The full Route needs to be provided to ensure
(either update or create) the Route. Non present data will
only be filled with defaults or left empty, but not take
previous values into consideration.


### Example

* Bearer (JWT) Authentication (tokenAuth):

```python
import ionoscloud_api_gateway
from ionoscloud_api_gateway.models.route_ensure import RouteEnsure
from ionoscloud_api_gateway.models.route_read import RouteRead
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
    api_instance = ionoscloud_api_gateway.RoutesApi(api_client)
    apigateway_id = '0620c174-dd3c-5eb4-87c8-e2b516553a00' # str | The ID (UUID) of the Gateway.
    route_id = '50982018-bb17-5cb9-bcd4-97f8bbc7dc23' # str | The ID (UUID) of the Route.
    route_ensure = ionoscloud_api_gateway.RouteEnsure() # RouteEnsure | update Route

    try:
        # Ensure Route
        api_response = api_instance.apigateways_routes_put(apigateway_id, route_id, route_ensure)
        print("The response of RoutesApi->apigateways_routes_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutesApi->apigateways_routes_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **apigateway_id** | **str**| The ID (UUID) of the Gateway. | 
 **route_id** | **str**| The ID (UUID) of the Route. | 
 **route_ensure** | [**RouteEnsure**](RouteEnsure.md)| update Route | 

### Return type

[**RouteRead**](RouteRead.md)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Route successfully updated. |  -  |
**201** | Route successfully ensured. |  -  |
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

