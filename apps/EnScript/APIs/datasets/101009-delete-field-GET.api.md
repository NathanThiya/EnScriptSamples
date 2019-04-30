# Delete a field from the dataset

When a field is deleted, the data in that field is not removed.
Even when a field is removed, the dataset will contain the data for that attribute
Field data has to be removed separately using en.data.sets.deleteFieldData API call


<% assign datasetId = 'test1000' %>                      // Mandatory
<% assign fieldId = 'firstName' %>                      // Mandatory

<% en.data.sets.deleteField results datasetId fieldId %>
<% return 'test1000-deleteField' results %>
