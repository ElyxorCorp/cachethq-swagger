# VersionMetaLatest


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tag_name** | **str** |  | [optional] 
**prelease** | **bool** |  | [optional] 
**draft** | **bool** |  | [optional] 

## Example

```python
from cachethq_client.models.version_meta_latest import VersionMetaLatest

# TODO update the JSON string below
json = "{}"
# create an instance of VersionMetaLatest from a JSON string
version_meta_latest_instance = VersionMetaLatest.from_json(json)
# print the JSON string representation of the object
print VersionMetaLatest.to_json()

# convert the object into a dict
version_meta_latest_dict = version_meta_latest_instance.to_dict()
# create an instance of VersionMetaLatest from a dict
version_meta_latest_form_dict = version_meta_latest.from_dict(version_meta_latest_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


