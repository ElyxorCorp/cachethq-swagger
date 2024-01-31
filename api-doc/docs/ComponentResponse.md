# ComponentResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**link** | **str** |  | [optional] 
**status** | **int** |  | [optional] 
**order** | **int** |  | [optional] 
**group_id** | **int** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 
**deleted_at** | **str** |  | [optional] 
**status_name** | **str** |  | [optional] 
**tags** | **Dict[str, object]** | Key-value pairs of tags where the key is the slug and the value is the name. | [optional] 

## Example

```python
from cachethq_client.models.component_response import ComponentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ComponentResponse from a JSON string
component_response_instance = ComponentResponse.from_json(json)
# print the JSON string representation of the object
print ComponentResponse.to_json()

# convert the object into a dict
component_response_dict = component_response_instance.to_dict()
# create an instance of ComponentResponse from a dict
component_response_form_dict = component_response.from_dict(component_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


