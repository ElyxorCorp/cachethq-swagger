# MetricPointsResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**metric_id** | **int** |  | [optional] 
**value** | **float** |  | [optional] 
**counter** | **int** |  | [optional] 
**calculated_value** | **float** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 

## Example

```python
from cachethq_client.models.metric_points_response import MetricPointsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MetricPointsResponse from a JSON string
metric_points_response_instance = MetricPointsResponse.from_json(json)
# print the JSON string representation of the object
print MetricPointsResponse.to_json()

# convert the object into a dict
metric_points_response_dict = metric_points_response_instance.to_dict()
# create an instance of MetricPointsResponse from a dict
metric_points_response_form_dict = metric_points_response.from_dict(metric_points_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


