# SingleMetricResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**MetricsResponse**](MetricsResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_metric_response import SingleMetricResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleMetricResponse from a JSON string
single_metric_response_instance = SingleMetricResponse.from_json(json)
# print the JSON string representation of the object
print SingleMetricResponse.to_json()

# convert the object into a dict
single_metric_response_dict = single_metric_response_instance.to_dict()
# create an instance of SingleMetricResponse from a dict
single_metric_response_form_dict = single_metric_response.from_dict(single_metric_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


