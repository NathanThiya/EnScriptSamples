# Find data from dataset

en.data.find or en.data.findMany - Find many rows that matches query
Always as a best practice return only the fields needed by your client application. 
This will increase the performance of the server and your application.
Don't return all fields which is the default behavior.

<% assign datasetId = 'test1000' %>         // Mandatory

<% assign query.name = 'John Doe' %>

Parameters
name | description
-----|------------
datasetId   | id of the dataset
query       | A find query Object
fields      | A fields query Object or a comma separated field ids.
orderBy     | An Object representing the sort order
pageSize    | How many items to return on the current page. Default: 25 Max:
page        | Current page number starts from 1.    Default: 1
omitIdField | true/false. This indicates whether to return _id field as part the returned result.

## Simple Query

### returns all fields
<% en.data.find results1 datasetId query fields %>
<% return 'test1000-one-1' results1 %>


### returns only requested fields
Fields can be defined as comma separated fields
<% assign fields = 'name,description' %>

### Fields can be defined as an Object as well
<% rem assign fields.name = 1 %>
<% rem assign fields.description = 1 %>
Refer to MongoDB query information for more details
(Mongo Query)[https://docs.mongodb.com/manual/reference/method/db.collection.find/]

<% en.data.find results2 datasetId query fields %>
<% return 'test1000-find-2' results2 %>

## Advanced queries

Refer to MongoDB query information for more advanced queries
(Mongo Query)[https://docs.mongodb.com/manual/reference/method/db.collection.find/]

Find searchText within name field or description field.

<% unassign query %>

<% assign searchText = 'john' %>
<% assign nameQuery.name.$regex = searchText %> // Regular expression
<% assign nameQuery.name.$options = '$i' %> // Regular expression case insensitive
<% assign descQuery.description.$regex = searchText %>
<% assign descQuery.description.$options = '$i' %>
<% assign query.$or = [nameQuery, descQuery] %> // Or query


<% assign query.name.$regex = 'John Doe' %>
<% assign fields = 'name,description' %>
<% en.data.find results3 datasetId query fields %>
<% return 'test1000-find-3' results3 %>

