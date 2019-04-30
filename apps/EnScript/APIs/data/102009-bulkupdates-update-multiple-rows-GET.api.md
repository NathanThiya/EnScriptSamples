# Bulk Update rows

en.data.bulkupdates results datasetId updateObjects idField 



results         | update results
datasetId       | id or _id of dataset
updateObjects   | Array of update object with the Id field
idField         | Optional By default idField is '_id', however this can be changed.


Example1:
<% assign updateObjects[0]._id = 'id of the object to be updated' %>
<% assign updateObjects[0].field1 = 'Updated value of field1' %>
<% assign updateObjects[0].name = 'Updated value of name' %>
<% assign updateObjects[0].description = 'Updated value of description' %>
<% assign updateObjects[0].teaser = 'Updated value of teaser' %>

<% assign updateObjects[1]._id = 'id of the object to be updated' %>
<% assign updateObjects[2].field1 = 'Updated value of field1' %>
<% assign updateObjects[3].name = 'Updated value of name' %>
<% assign updateObjects[4].description = 'Updated value of description' %>
<% assign updateObjects[5].teaser = 'Updated value of teaser' %>

<% en.data.bulkupdates results datasetId updateObjects  %>