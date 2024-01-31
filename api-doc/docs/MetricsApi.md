# cachethq_client.MetricsApi

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_metric**](MetricsApi.md#create_metric) | **POST** /metrics | Create a metric
[**create_metric_point_by_id**](MetricsApi.md#create_metric_point_by_id) | **POST** /metrics/{metric}/points | Create point for a metric
[**delete_metric_by_id**](MetricsApi.md#delete_metric_by_id) | **DELETE** /metrics/{metric} | Delete a metric
[**delete_metric_point_by_id**](MetricsApi.md#delete_metric_point_by_id) | **DELETE** /metrics/{metric}/points/{point} | Delete a metric point
[**get_metric_by_id**](MetricsApi.md#get_metric_by_id) | **GET** /metrics/{metric} | Get a metric
[**get_metric_points_by_id**](MetricsApi.md#get_metric_points_by_id) | **GET** /metrics/{metric}/points | Get points for a metric
[**get_metrics**](MetricsApi.md#get_metrics) | **GET** /metrics | Get all metrics


# **create_metric**
> SingleMetricResponse create_metric(body)

Create a metric

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.metric import Metric
from cachethq_client.models.single_metric_response import SingleMetricResponse
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
    api_instance = cachethq_client.MetricsApi(api_client)
    body = cachethq_client.Metric() # Metric | Create metric data

    try:
        # Create a metric
        api_response = api_instance.create_metric(body)
        print("The response of MetricsApi->create_metric:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->create_metric: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Metric**](Metric.md)| Create metric data | 

### Return type

[**SingleMetricResponse**](SingleMetricResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Create metric response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_metric_point_by_id**
> SingleMetricPointResponse create_metric_point_by_id(metric, body)

Create point for a metric

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.metric_point import MetricPoint
from cachethq_client.models.single_metric_point_response import SingleMetricPointResponse
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
    api_instance = cachethq_client.MetricsApi(api_client)
    metric = 56 # int | Unique metric id
    body = cachethq_client.MetricPoint() # MetricPoint | Metric data

    try:
        # Create point for a metric
        api_response = api_instance.create_metric_point_by_id(metric, body)
        print("The response of MetricsApi->create_metric_point_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->create_metric_point_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metric** | **int**| Unique metric id | 
 **body** | [**MetricPoint**](MetricPoint.md)| Metric data | 

### Return type

[**SingleMetricPointResponse**](SingleMetricPointResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Create metric point response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_metric_by_id**
> str delete_metric_by_id(metric)

Delete a metric

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
    api_instance = cachethq_client.MetricsApi(api_client)
    metric = 56 # int | Unique metric id

    try:
        # Delete a metric
        api_response = api_instance.delete_metric_by_id(metric)
        print("The response of MetricsApi->delete_metric_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->delete_metric_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metric** | **int**| Unique metric id | 

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
**200** | Delete metric response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_metric_point_by_id**
> str delete_metric_point_by_id(metric, point)

Delete a metric point

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
    api_instance = cachethq_client.MetricsApi(api_client)
    metric = 56 # int | Unique metric id
    point = 56 # int | Unique metric point id

    try:
        # Delete a metric point
        api_response = api_instance.delete_metric_point_by_id(metric, point)
        print("The response of MetricsApi->delete_metric_point_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->delete_metric_point_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metric** | **int**| Unique metric id | 
 **point** | **int**| Unique metric point id | 

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
**200** | Delete metric point response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_metric_by_id**
> SingleMetricResponse get_metric_by_id(metric)

Get a metric

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.single_metric_response import SingleMetricResponse
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
    api_instance = cachethq_client.MetricsApi(api_client)
    metric = 56 # int | Unique metric id

    try:
        # Get a metric
        api_response = api_instance.get_metric_by_id(metric)
        print("The response of MetricsApi->get_metric_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->get_metric_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metric** | **int**| Unique metric id | 

### Return type

[**SingleMetricResponse**](SingleMetricResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get metric response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_metric_points_by_id**
> ListMetricPointsResponse get_metric_points_by_id(metric, sort=sort, order=order, per_page=per_page, page=page)

Get points for a metric

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.list_metric_points_response import ListMetricPointsResponse
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
    api_instance = cachethq_client.MetricsApi(api_client)
    metric = 56 # int | Unique metric id
    sort = 'id' # str | Object property to filter on. (optional) (default to 'id')
    order = 'asc' # str | Ordering parameter with options of asc or desc. (optional) (default to 'asc')
    per_page = 56 # int | Results per page. (optional)
    page = 56 # int |  (optional)

    try:
        # Get points for a metric
        api_response = api_instance.get_metric_points_by_id(metric, sort=sort, order=order, per_page=per_page, page=page)
        print("The response of MetricsApi->get_metric_points_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->get_metric_points_by_id: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **metric** | **int**| Unique metric id | 
 **sort** | **str**| Object property to filter on. | [optional] [default to &#39;id&#39;]
 **order** | **str**| Ordering parameter with options of asc or desc. | [optional] [default to &#39;asc&#39;]
 **per_page** | **int**| Results per page. | [optional] 
 **page** | **int**|  | [optional] 

### Return type

[**ListMetricPointsResponse**](ListMetricPointsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get metric points response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_metrics**
> ListMetricsResponse get_metrics(sort=sort, order=order, per_page=per_page, page=page)

Get all metrics

### Example

* Api Key Authentication (apiKey):
```python
import time
import os
import cachethq_client
from cachethq_client.models.list_metrics_response import ListMetricsResponse
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
    api_instance = cachethq_client.MetricsApi(api_client)
    sort = 'id' # str | Object property to filter on. (optional) (default to 'id')
    order = 'asc' # str | Ordering parameter with options of asc or desc. (optional) (default to 'asc')
    per_page = 56 # int | Results per page. (optional)
    page = 56 # int |  (optional)

    try:
        # Get all metrics
        api_response = api_instance.get_metrics(sort=sort, order=order, per_page=per_page, page=page)
        print("The response of MetricsApi->get_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetricsApi->get_metrics: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sort** | **str**| Object property to filter on. | [optional] [default to &#39;id&#39;]
 **order** | **str**| Ordering parameter with options of asc or desc. | [optional] [default to &#39;asc&#39;]
 **per_page** | **int**| Results per page. | [optional] 
 **page** | **int**|  | [optional] 

### Return type

[**ListMetricsResponse**](ListMetricsResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Get metrics response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

