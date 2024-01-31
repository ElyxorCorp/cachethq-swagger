# ListMetricPointsResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta** | [**MetaData**](MetaData.md) |  | [optional] 
**data** | [**List[MetricPointsResponse]**](MetricPointsResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.list_metric_points_response import ListMetricPointsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListMetricPointsResponse from a JSON string
list_metric_points_response_instance = ListMetricPointsResponse.from_json(json)
# print the JSON string representation of the object
print ListMetricPointsResponse.to_json()

# convert the object into a dict
list_metric_points_response_dict = list_metric_points_response_instance.to_dict()
# create an instance of ListMetricPointsResponse from a dict
list_metric_points_response_form_dict = list_metric_points_response.from_dict(list_metric_points_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


