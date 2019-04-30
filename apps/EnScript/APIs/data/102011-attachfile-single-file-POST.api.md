# Attache a file to a datarow.

en.data.attachFile

This API will allow 


en.data.attachFile results datasetId fieldId rowId isPrivate file
en.data.uploadFile results datasetId fieldId rowId isPrivate file


results 
datasetId       | id or _id of the dataset
fieldId         | id of the field. This field must be defined in the dataset and its data type must be FILE or IMAGE. If the field's isArray=true, the file will be stored as an array.
rowId           | datarow's id field
isPrivate       | if this is true, it will override the isPrivate settings on the dataset field.
file


Every attached file or image will have url regardless of private or public.
If the file is private by default only the owner of attachment will have access to the file.
Any available roles can be granted permissions to the field by setting the field roles. roles is an Array.

When attaching a file, the field must be empty. If the field has any values, file upload will fail.

Example:
<% assign datasetId = 'test1000' %>
<% rem assign fieldId = 'files' %>
<% assign fieldId = 'publicfile' %>
<% assign rowId = '3ca11iz8em-5108c3b6-e300-4620-b4b7-18361501875b' %>

<% if en.req.hasFile %>
    <% return 'hasFile' 'yes' %>
    <% en.data.attachfile results datasetId  fieldId rowId %>
    <% return results  %>
<% else %>
    <% return 'hasFile' 'no' %>
    <% return 'error' 'No files found' %>
<% endif %>

