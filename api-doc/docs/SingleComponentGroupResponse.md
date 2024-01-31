# SingleComponentGroupResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**ComponentGroupResponse**](ComponentGroupResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_component_group_response import SingleComponentGroupResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleComponentGroupResponse from a JSON string
single_component_group_response_instance = SingleComponentGroupResponse.from_json(json)
# print the JSON string representation of the object
print SingleComponentGroupResponse.to_json()

# convert the object into a dict
single_component_group_response_dict = single_component_group_response_instance.to_dict()
# create an instance of SingleComponentGroupResponse from a dict
single_component_group_response_form_dict = single_component_group_response.from_dict(single_component_group_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


