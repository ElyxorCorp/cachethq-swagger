# SingleIncidentUpdateResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**IncidentUpdateResponse**](IncidentUpdateResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_incident_update_response import SingleIncidentUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleIncidentUpdateResponse from a JSON string
single_incident_update_response_instance = SingleIncidentUpdateResponse.from_json(json)
# print the JSON string representation of the object
print SingleIncidentUpdateResponse.to_json()

# convert the object into a dict
single_incident_update_response_dict = single_incident_update_response_instance.to_dict()
# create an instance of SingleIncidentUpdateResponse from a dict
single_incident_update_response_form_dict = single_incident_update_response.from_dict(single_incident_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


