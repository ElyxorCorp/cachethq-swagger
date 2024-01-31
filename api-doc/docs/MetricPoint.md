# MetricPoint


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **float** |  | [optional] 
**timestamp** | **str** |  | [optional] 

## Example

```python
from cachethq_client.models.metric_point import MetricPoint

# TODO update the JSON string below
json = "{}"
# create an instance of MetricPoint from a JSON string
metric_point_instance = MetricPoint.from_json(json)
# print the JSON string representation of the object
print MetricPoint.to_json()

# convert the object into a dict
metric_point_dict = metric_point_instance.to_dict()
# create an instance of MetricPoint from a dict
metric_point_form_dict = metric_point.from_dict(metric_point_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


