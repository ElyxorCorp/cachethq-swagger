# SingleIncidentResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**IncidentResponse**](IncidentResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.single_incident_response import SingleIncidentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SingleIncidentResponse from a JSON string
single_incident_response_instance = SingleIncidentResponse.from_json(json)
# print the JSON string representation of the object
print SingleIncidentResponse.to_json()

# convert the object into a dict
single_incident_response_dict = single_incident_response_instance.to_dict()
# create an instance of SingleIncidentResponse from a dict
single_incident_response_form_dict = single_incident_response.from_dict(single_incident_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


