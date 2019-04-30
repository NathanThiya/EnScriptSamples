// en.data.updateMany or en.data.updateMongo
// This API allows user to update multiple rows that matches the query at the same time.

<% assign query.name = 'John Doe' %>

//              - updatedRow can also contain any MongoDB update Document with any of the mongo db update operations.
//                    https://docs.mongodb.com/manual/reference/operator/update/

// results      - In case of using complex MongoDB updates, the row returned with results will not have all the updates sent with operators.
//              - Only $set operator changes will be in the returned results.
// 


<% assign datasetId = 'test1000' %>                      // Mandatory

<% assign updatedRow.$inc.views = 1 %>
<% assign updatedRow.$addToSet.tags = 'TAG1' %>
<% assign updatedRow.$set.description = 'Some description will go here - Updated 3' %>

<% en.data.updateMany results2 datasetId query updatedRow %>
<% return 'test1000-update-data-2' results2 %>

