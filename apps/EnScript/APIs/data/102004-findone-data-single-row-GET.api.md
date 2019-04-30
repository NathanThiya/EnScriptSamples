# Find data - Single row from a dataset

en.data.findOne - Find a single row that matches query.
If the query matches multiple rows, only the first row will be returned.
The first row is not predictable.

<% assign datasetId = 'test1000' %>                      // Mandatory

<% assign query.name = 'John Doe' %>

Parameters

Name    | Description
--------|-------------
datasetId   | id or _id of the dataset
query       | A find query Object
fields      | A fields query Object or a comma separated field ids

### Returns all fields
<% en.data.findOne results1 datasetId query fields %>
<% return 'test1000-find-one-1' results1 %>


### Returns only requested fields
<% assign fields = 'name,description' %>
<% en.data.findOne results2 datasetId query fields %>
<% return 'test1000-find-one-2' results2 %>

