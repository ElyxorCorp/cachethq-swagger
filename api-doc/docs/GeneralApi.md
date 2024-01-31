# cachethq_client.GeneralApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ping**](GeneralApi.md#ping) | **GET** /ping | Test that the API is responding to your requests.
[**version**](GeneralApi.md#version) | **GET** /version | Get the Cachet version.


# **ping**
> Ping ping()

Test that the API is responding to your requests.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.ping import Ping
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
    api_instance = cachethq_client.GeneralApi(api_client)

    try:
        # Test that the API is responding to your requests.
        api_response = api_instance.ping()
        print("The response of GeneralApi->ping:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GeneralApi->ping: %s\n" % e)
```



### Parameters
This endpoint does not need any parameter.

### Return type

[**Ping**](Ping.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ping response |  -  |
**0** | Unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **version**
> Version version()

Get the Cachet version.

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.version import Version
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
    api_instance = cachethq_client.GeneralApi(api_client)

    try:
        # Get the Cachet version.
        api_response = api_instance.version()
        print("The response of GeneralApi->version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling GeneralApi->version: %s\n" % e)
```



### Parameters
This endpoint does not need any parameter.

### Return type

[**Version**](Version.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Version response |  -  |
**0** | Unexpected error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

