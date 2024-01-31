# IncidentUpdateResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**incident_id** | **int** |  | [optional] 
**status** | **int** |  | [optional] 
**message** | **str** |  | [optional] 
**user_id** | **int** |  | [optional] 
**created_at** | **str** |  | [optional] 
**updated_at** | **str** |  | [optional] 
**human_status** | **str** |  | [optional] 
**permalink** | **str** |  | [optional] 

## Example

```python
from cachethq_client.models.incident_update_response import IncidentUpdateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IncidentUpdateResponse from a JSON string
incident_update_response_instance = IncidentUpdateResponse.from_json(json)
# print the JSON string representation of the object
print IncidentUpdateResponse.to_json()

# convert the object into a dict
incident_update_response_dict = incident_update_response_instance.to_dict()
# create an instance of IncidentUpdateResponse from a dict
incident_update_response_form_dict = incident_update_response.from_dict(incident_update_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


