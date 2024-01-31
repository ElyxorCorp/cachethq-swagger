# cachethq_client.IncidentsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_incident**](IncidentsApi.md#create_incident) | **POST** /incidents | Create a new incident.
[**delete_incident_by_id**](IncidentsApi.md#delete_incident_by_id) | **DELETE** /incidents/{incident} | Delete an incident
[**get_incident_by_id**](IncidentsApi.md#get_incident_by_id) | **GET** /incidents/{incident} | Get an incident
[**get_incident_updates_by_id**](IncidentsApi.md#get_incident_updates_by_id) | **GET** /incidents/{incident}/updates | Get incident updates
[**get_incidents**](IncidentsApi.md#get_incidents) | **GET** /incidents | Get all incidents.
[**update_incident_by_id**](IncidentsApi.md#update_incident_by_id) | **PUT** /incidents/{incident} | Update an incident


# **create_incident**
> SingleIncidentResponse create_incident(body)

Create a new incident.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.incident import Incident
from cachethq_client.models.single_incident_response import SingleIncidentResponse
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
    api_instance = cachethq_client.IncidentsApi(api_client)
    body = cachethq_client.Incident() # Incident | Incident to be created

    try:
        # Create a new incident.
        api_response = api_instance.create_incident(body)
        print("The response of IncidentsApi->create_incident:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->create_incident: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Incident**](Incident.md)| Incident to be created | 

### Return type

[**SingleIncidentResponse**](SingleIncidentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Incident created response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_incident_by_id**
> str delete_incident_by_id(incident)

Delete an incident

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
    api_instance = cachethq_client.IncidentsApi(api_client)
    incident = 56 # int | Unique incident id

    try:
        # Delete an incident
        api_response = api_instance.delete_incident_by_id(incident)
        print("The response of IncidentsApi->delete_incident_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->delete_incident_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **incident** | **int**| Unique incident id | 

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
**200** | Delete incident response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_incident_by_id**
> SingleIncidentResponse get_incident_by_id(incident)

Get an incident

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.single_incident_response import SingleIncidentResponse
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
    api_instance = cachethq_client.IncidentsApi(api_client)
    incident = 56 # int | Unique incident id

    try:
        # Get an incident
        api_response = api_instance.get_incident_by_id(incident)
        print("The response of IncidentsApi->get_incident_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->get_incident_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **incident** | **int**| Unique incident id | 

### Return type

[**SingleIncidentResponse**](SingleIncidentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get incident response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_incident_updates_by_id**
> ListIncidentUpdatesResponse get_incident_updates_by_id(incident, sort=sort, order=order, per_page=per_page, page=page)

Get incident updates

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.list_incident_updates_response import ListIncidentUpdatesResponse
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
    api_instance = cachethq_client.IncidentsApi(api_client)
    incident = 56 # int | Unique incident id
    sort = 'id' # str | Object property to filter on. (optional) (default to 'id')
    order = 'asc' # str | Ordering parameter with options of asc or desc. (optional) (default to 'asc')
    per_page = 56 # int | Results per page. (optional)
    page = 56 # int |  (optional)

    try:
        # Get incident updates
        api_response = api_instance.get_incident_updates_by_id(incident, sort=sort, order=order, per_page=per_page, page=page)
        print("The response of IncidentsApi->get_incident_updates_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->get_incident_updates_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **incident** | **int**| Unique incident id | 
 **sort** | **str**| Object property to filter on. | [optional] [default to &#39;id&#39;]
 **order** | **str**| Ordering parameter with options of asc or desc. | [optional] [default to &#39;asc&#39;]
 **per_page** | **int**| Results per page. | [optional] 
 **page** | **int**|  | [optional] 

### Return type

[**ListIncidentUpdatesResponse**](ListIncidentUpdatesResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get incident updates response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_incidents**
> ListIncidentsResponse get_incidents(id=id, component_id=component_id, name=name, status=status, visible=visible, sort=sort, order=order, per_page=per_page, page=page)

Get all incidents.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.list_incidents_response import ListIncidentsResponse
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
    api_instance = cachethq_client.IncidentsApi(api_client)
    id = 56 # int | Unique incident id (optional)
    component_id = 56 # int | Unique component group id (optional)
    name = 'name_example' # str | Full or partial component group name (optional)
    status = 56 # int |  (optional)
    visible = 3.4 # float |  (optional)
    sort = 'id' # str | Object property to filter on. (optional) (default to 'id')
    order = 'asc' # str | Ordering parameter with options of asc or desc. (optional) (default to 'asc')
    per_page = 56 # int | Results per page. (optional)
    page = 56 # int |  (optional)

    try:
        # Get all incidents.
        api_response = api_instance.get_incidents(id=id, component_id=component_id, name=name, status=status, visible=visible, sort=sort, order=order, per_page=per_page, page=page)
        print("The response of IncidentsApi->get_incidents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->get_incidents: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| Unique incident id | [optional] 
 **component_id** | **int**| Unique component group id | [optional] 
 **name** | **str**| Full or partial component group name | [optional] 
 **status** | **int**|  | [optional] 
 **visible** | **float**|  | [optional] 
 **sort** | **str**| Object property to filter on. | [optional] [default to &#39;id&#39;]
 **order** | **str**| Ordering parameter with options of asc or desc. | [optional] [default to &#39;asc&#39;]
 **per_page** | **int**| Results per page. | [optional] 
 **page** | **int**|  | [optional] 

### Return type

[**ListIncidentsResponse**](ListIncidentsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get incidents response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_incident_by_id**
> SingleIncidentResponse update_incident_by_id(incident, body)

Update an incident

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.incident import Incident
from cachethq_client.models.single_incident_response import SingleIncidentResponse
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
    api_instance = cachethq_client.IncidentsApi(api_client)
    incident = 56 # int | Unique incident id
    body = cachethq_client.Incident() # Incident | Incident data to be updated

    try:
        # Update an incident
        api_response = api_instance.update_incident_by_id(incident, body)
        print("The response of IncidentsApi->update_incident_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IncidentsApi->update_incident_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **incident** | **int**| Unique incident id | 
 **body** | [**Incident**](Incident.md)| Incident data to be updated | 

### Return type

[**SingleIncidentResponse**](SingleIncidentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Update incident response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

