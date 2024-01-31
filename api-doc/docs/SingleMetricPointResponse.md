# SingleMetricPointResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**MetricPointsResponse**](MetricPointsResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_metric_point_response import SingleMetricPointResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleMetricPointResponse from a JSON string
single_metric_point_response_instance = SingleMetricPointResponse.from_json(json)
# print the JSON string representation of the object
print SingleMetricPointResponse.to_json()

# convert the object into a dict
single_metric_point_response_dict = single_metric_point_response_instance.to_dict()
# create an instance of SingleMetricPointResponse from a dict
single_metric_point_response_form_dict = single_metric_point_response.from_dict(single_metric_point_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


