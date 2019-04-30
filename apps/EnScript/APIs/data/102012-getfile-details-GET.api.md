# Get File

Get file API is used to get the file details as JSON or DOWNLOAD or VIEW


en.data.getfile results datasetId  fieldId rowId attachmentId action



results         | results of the API
datasetId       | id or _id of a dataset
fieldId         | id of the field
rowId           | data row's _id field value of the attachment file
attachmentId    | _id field of the attachment.
action          | valid values are: VIEW, DOWNLOAD, JSON


Example #1:

<% assign datasetId = en.uri.5 %>
<% assign rowId = en.uri.6 %>
<% assign fieldId = en.uri.7 %>
<% assign attachmentId = en.uri.8 %>
<% assign action = en.uri.9 %> //Valid actions are: view or download. If the action is empty, it will give JSON result.

<% return 'datasetId' datasetId %>
<% return 'rowId' rowId %>
<% return 'fieldId' fieldId %>
<% return 'attachmentId' attachmentId %>
<% en.data.getfile results datasetId  fieldId rowId attachmentId action %>
<% return results %>
<% return 'getfile' true %>
<% end %>
