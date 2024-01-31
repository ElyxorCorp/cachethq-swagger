# ComponentGroup


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**order** | **int** |  | [optional] 
**collapsed** | **int** |  | [optional] 

## Example

```python
from cachethq_client.models.component_group import ComponentGroup

# TODO update the JSON string below
json = "{}"
# create an instance of ComponentGroup from a JSON string
component_group_instance = ComponentGroup.from_json(json)
# print the JSON string representation of the object
print ComponentGroup.to_json()

# convert the object into a dict
component_group_dict = component_group_instance.to_dict()
# create an instance of ComponentGroup from a dict
component_group_form_dict = component_group.from_dict(component_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


