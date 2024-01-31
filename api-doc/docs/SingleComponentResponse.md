# SingleComponentResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**ComponentResponse**](ComponentResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_component_response import SingleComponentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleComponentResponse from a JSON string
single_component_response_instance = SingleComponentResponse.from_json(json)
# print the JSON string representation of the object
print SingleComponentResponse.to_json()

# convert the object into a dict
single_component_response_dict = single_component_response_instance.to_dict()
# create an instance of SingleComponentResponse from a dict
single_component_response_form_dict = single_component_response.from_dict(single_component_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


