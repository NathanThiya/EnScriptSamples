# Update Single Row data to a dataset
// All APIs starts with en.db.* is deprecated. Do not use these APIs.

en.data.update will only update single row (Document)
If the query matches more than one rows, only the first row will be updated. First row is not predicatable and random.

## Updating with simple document object with multiple attributes

<% assign datasetId = 'test1000' %>                      // Mandatory

<% assign query.name = 'John Doe' %>

<% assign updatedRow.description = 'Some description will go here - Updated' %>

Parameters
Name | Description
-----|------------
results     | In case of simple updates, returned results row will be updated with the values that needs to be updated
datasetId   | data set to update
query       | Query can be a MongoDB Query object to find one or more records.
            | Any records that matches the above query will be updated.
            | Remember en.data.update will only update 1 row, if the query finds multiple rows.
query       | Query can also be a string value from '_id' field or 'id' field
            | Any record that matches the above _id field or id field will be updated
updatedRow  | Updated Row must be a Document Object
            | Updated Row can be simple Document Object that has attributes to update
            | _id cannot be updated. This will result in error

<% en.data.update results datasetId query updatedRow %>
<% return 'test1000-update-data' results %>


2. Advanced Updating with MongoDB Operators
    In this update the row returned 

Unassign will remove the object from memory.
<% unassign updatedRow %>

<% assign query.name = 'John Doe' %>

updatedRow can also contain any MongoDB update Document with any of the mongo db update operations.
[MongoDB Update](https://docs.mongodb.com/manual/reference/operator/update/)

// results      - In case of using complex MongoDB updates, the row returned with results will not have all the updates sent with operators.
//              - Only $set operator changes will be in the returned results.
// 

<% assign updatedRow.$inc.views = 1 %>
<% assign updatedRow.$push.tags = 'TAG1' %>
<% assign updatedRow.$set.description = 'Some description will go here - Updated 2' %>

<% en.data.update results2 datasetId query updatedRow %>
<% return 'test1000-update-data-2' results2 %>

