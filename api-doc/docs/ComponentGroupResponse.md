# ComponentGroupResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**name** | **str** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 
**order** | **int** |  | [optional] 
**collapsed** | **float** |  | [optional] 
**visible** | **float** |  | [optional] 
**enabled_components** | [**List[ComponentResponse]**](ComponentResponse.md) |  | [optional] 
**enabled_components_lowest** | [**List[ComponentResponse]**](ComponentResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.component_group_response import ComponentGroupResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ComponentGroupResponse from a JSON string
component_group_response_instance = ComponentGroupResponse.from_json(json)
# print the JSON string representation of the object
print ComponentGroupResponse.to_json()

# convert the object into a dict
component_group_response_dict = component_group_response_instance.to_dict()
# create an instance of ComponentGroupResponse from a dict
component_group_response_form_dict = component_group_response.from_dict(component_group_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


