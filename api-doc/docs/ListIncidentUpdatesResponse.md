# ListIncidentUpdatesResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta** | [**MetaData**](MetaData.md) |  | [optional] 
**data** | [**List[IncidentUpdateResponse]**](IncidentUpdateResponse.md) |  | [optional] 

## Example

```python
from cachethq_client.models.list_incident_updates_response import ListIncidentUpdatesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListIncidentUpdatesResponse from a JSON string
list_incident_updates_response_instance = ListIncidentUpdatesResponse.from_json(json)
# print the JSON string representation of the object
print ListIncidentUpdatesResponse.to_json()

# convert the object into a dict
list_incident_updates_response_dict = list_incident_updates_response_instance.to_dict()
# create an instance of ListIncidentUpdatesResponse from a dict
list_incident_updates_response_form_dict = list_incident_updates_response.from_dict(list_incident_updates_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


