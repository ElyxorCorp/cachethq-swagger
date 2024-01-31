# ListComponentGroupsResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta** | [**MetaData**](MetaData.md) |  | [optional] 
**data** | [**List[ComponentGroupResponse]**](ComponentGroupResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.list_component_groups_response import ListComponentGroupsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListComponentGroupsResponse from a JSON string
list_component_groups_response_instance = ListComponentGroupsResponse.from_json(json)
# print the JSON string representation of the object
print ListComponentGroupsResponse.to_json()

# convert the object into a dict
list_component_groups_response_dict = list_component_groups_response_instance.to_dict()
# create an instance of ListComponentGroupsResponse from a dict
list_component_groups_response_form_dict = list_component_groups_response.from_dict(list_component_groups_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


