# Incident


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**status** | **int** |  | [optional] 
**visible** | **int** |  | [optional] 
**component_id** | **int** |  | [optional] 
**component_status** | **int** |  | [optional] 
**notify** | **float** |  | [optional] 
**created_at** | **str** |  | [optional] 
**template** | **str** |  | [optional] 
**vars** | **object** |  | [optional] 

## Example

```python
from cachethq_client.models.incident import Incident

# TODO update the JSON string below
json = "{}"
# create an instance of Incident from a JSON string
incident_instance = Incident.from_json(json)
# print the JSON string representation of the object
print Incident.to_json()

# convert the object into a dict
incident_dict = incident_instance.to_dict()
# create an instance of Incident from a dict
incident_form_dict = incident.from_dict(incident_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


