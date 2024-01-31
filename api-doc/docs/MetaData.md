# MetaData


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 

## Example

```python
from cachethq_client.models.meta_data import MetaData

# TODO update the JSON string below
json = "{}"
# create an instance of MetaData from a JSON string
meta_data_instance = MetaData.from_json(json)
# print the JSON string representation of the object
print MetaData.to_json()

# convert the object into a dict
meta_data_dict = meta_data_instance.to_dict()
# create an instance of MetaData from a dict
meta_data_form_dict = meta_data.from_dict(meta_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


