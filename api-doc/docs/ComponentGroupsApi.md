# cachethq_client.ComponentGroupsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_component_group**](ComponentGroupsApi.md#create_component_group) | **POST** /components/groups | Create a new Component Group.
[**delete_component_group_by_id**](ComponentGroupsApi.md#delete_component_group_by_id) | **DELETE** /components/groups/{group} | Delete a Component Group.
[**get_component_group_by_id**](ComponentGroupsApi.md#get_component_group_by_id) | **GET** /components/groups/{group} | Get a Component Group.
[**get_component_groups**](ComponentGroupsApi.md#get_component_groups) | **GET** /components/groups | Get all Component Groups.
[**update_component_group_by_id**](ComponentGroupsApi.md#update_component_group_by_id) | **PUT** /components/groups/{group} | Update a Component Group.


# **create_component_group**
> SingleComponentGroupResponse create_component_group(body)

Create a new Component Group.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.component_group import ComponentGroup
from cachethq_client.models.single_component_group_response import SingleComponentGroupResponse
from cachethq_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cachethq_client.Configuration(
    host = "/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with cachethq_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cachethq_client.ComponentGroupsApi(api_client)
    body = cachethq_client.ComponentGroup() # ComponentGroup | Component Group to be created.

    try:
        # Create a new Component Group.
        api_response = api_instance.create_component_group(body)
        print("The response of ComponentGroupsApi->create_component_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComponentGroupsApi->create_component_group: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ComponentGroup**](ComponentGroup.md)| Component Group to be created. | 

### Return type

[**SingleComponentGroupResponse**](SingleComponentGroupResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Create component group response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_component_group_by_id**
> str delete_component_group_by_id(group)

Delete a Component Group.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cachethq_client.Configuration(
    host = "/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with cachethq_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cachethq_client.ComponentGroupsApi(api_client)
    group = 56 # int | Unique component group id

    try:
        # Delete a Component Group.
        api_response = api_instance.delete_component_group_by_id(group)
        print("The response of ComponentGroupsApi->delete_component_group_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComponentGroupsApi->delete_component_group_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **int**| Unique component group id | 

### Return type

**str**

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Delete component group response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_group_by_id**
> SingleComponentGroupResponse get_component_group_by_id(group)

Get a Component Group.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.single_component_group_response import SingleComponentGroupResponse
from cachethq_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cachethq_client.Configuration(
    host = "/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with cachethq_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cachethq_client.ComponentGroupsApi(api_client)
    group = 56 # int | Unique component group id

    try:
        # Get a Component Group.
        api_response = api_instance.get_component_group_by_id(group)
        print("The response of ComponentGroupsApi->get_component_group_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComponentGroupsApi->get_component_group_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **int**| Unique component group id | 

### Return type

[**SingleComponentGroupResponse**](SingleComponentGroupResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get a component group |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_component_groups**
> ListComponentGroupsResponse get_component_groups(id=id, name=name, collapsed=collapsed, sort=sort, order=order, per_page=per_page, page=page)

Get all Component Groups.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.list_component_groups_response import ListComponentGroupsResponse
from cachethq_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cachethq_client.Configuration(
    host = "/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with cachethq_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cachethq_client.ComponentGroupsApi(api_client)
    id = 56 # int | Unique component group id (optional)
    name = 'name_example' # str | Full or partial component group name (optional)
    collapsed = 3.4 # float | Group collapsed or not. (optional)
    sort = 'id' # str | Object property to filter on. (optional) (default to 'id')
    order = 'asc' # str | Ordering parameter with options of asc or desc. (optional) (default to 'asc')
    per_page = 56 # int | Results per page. (optional)
    page = 56 # int |  (optional)

    try:
        # Get all Component Groups.
        api_response = api_instance.get_component_groups(id=id, name=name, collapsed=collapsed, sort=sort, order=order, per_page=per_page, page=page)
        print("The response of ComponentGroupsApi->get_component_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComponentGroupsApi->get_component_groups: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Unique component group id | [optional] 
 **name** | **str**| Full or partial component group name | [optional] 
 **collapsed** | **float**| Group collapsed or not. | [optional] 
 **sort** | **str**| Object property to filter on. | [optional] [default to &#39;id&#39;]
 **order** | **str**| Ordering parameter with options of asc or desc. | [optional] [default to &#39;asc&#39;]
 **per_page** | **int**| Results per page. | [optional] 
 **page** | **int**|  | [optional] 

### Return type

[**ListComponentGroupsResponse**](ListComponentGroupsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get component groups response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_component_group_by_id**
> SingleComponentGroupResponse update_component_group_by_id(group, body)

Update a Component Group.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.component_group import ComponentGroup
from cachethq_client.models.single_component_group_response import SingleComponentGroupResponse
from cachethq_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to /api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = cachethq_client.Configuration(
    host = "/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure API key authorization: apiKey
configuration.api_key['apiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['apiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with cachethq_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = cachethq_client.ComponentGroupsApi(api_client)
    group = 56 # int | Unique component group id
    body = cachethq_client.ComponentGroup() # ComponentGroup | Component Group data to be updated

    try:
        # Update a Component Group.
        api_response = api_instance.update_component_group_by_id(group, body)
        print("The response of ComponentGroupsApi->update_component_group_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComponentGroupsApi->update_component_group_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group** | **int**| Unique component group id | 
 **body** | [**ComponentGroup**](ComponentGroup.md)| Component Group data to be updated | 

### Return type

[**SingleComponentGroupResponse**](SingleComponentGroupResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Update component group response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

