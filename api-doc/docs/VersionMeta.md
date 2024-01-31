# VersionMeta


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**on_latest** | **bool** |  | [optional] 
**latest** | [**VersionMetaLatest**](VersionMetaLatest.md) |  | [optional] 

## Example

```python
from cachethq_client.models.version_meta import VersionMeta

# TODO update the JSON string below
json = "{}"
# create an instance of VersionMeta from a JSON string
version_meta_instance = VersionMeta.from_json(json)
# print the JSON string representation of the object
print VersionMeta.to_json()

# convert the object into a dict
version_meta_dict = version_meta_instance.to_dict()
# create an instance of VersionMeta from a dict
version_meta_form_dict = version_meta.from_dict(version_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


