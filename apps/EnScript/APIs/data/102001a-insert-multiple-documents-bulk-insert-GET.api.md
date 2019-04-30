# Bulk Insert rows

en.data.bulkInsert results datasetId insertObjects



results         | insert results
datasetId       | id or _id of dataset
insertObjects   | Array of insert object with the Id field


Example1:
<% assign insertObjects[0]._id = 'id of the object to be inserted' %>
<% assign insertObjects[0].field1 = 'inserted value of field1' %>
<% assign insertObjects[0].name = 'inserted value of name' %>
<% assign insertObjects[0].description = 'inserted value of description' %>
<% assign insertObjects[0].teaser = 'inserted value of teaser' %>

<% assign insertObjects[1]._id = 'id of the object to be inserted' %>
<% assign insertObjects[2].field1 = 'inserted value of field1' %>
<% assign insertObjects[3].name = 'inserted value of name' %>
<% assign insertObjects[4].description = 'inserted value of description' %>
<% assign insertObjects[5].teaser = 'inserted value of teaser' %>

<% en.data.bulkInsert results datasetId insertObjects %>
