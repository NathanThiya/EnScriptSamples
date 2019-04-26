# Update a field on the dataset

Field id and field dataType cannot be changed when updating.

<% assign datasetId = 'test1000' %>                             // Mandatory
<% assign fieldId = 'firstName' %>                              // Mandatory


Updated Field Information
<% assign field.name        = 'First Name - Updated' %>         // Mandatory
<% assign field.uiType      = 'TEXTAREA' %>                     // Optional, default:TEXTBOX

<% en.data.sets.updateField results datasetId fieldId field %>
<% return 'test1000-updateField' results %>
