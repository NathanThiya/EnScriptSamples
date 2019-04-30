# Find distinct values from field within a dataset.


This API helps to find distinct values that are stored within full dataset or a filtered sub dataset.

Distinct API must be called with correct datatype.
There are 5 different APIs available to perform a distinct on a field based on the data type.

en.data.distinctString
en.data.distinctInteger
en.data.distinctLong
en.data.distinctDouble
en.data.distinctDate

en.data.distinctString results datasetId fieldId query


Name        | Description
------------|-------------
results     | This APIs results will be returned here.
datasetId   | id or _id of dataset 
fieldId     | field id of where the file is stored
query       | Query to filter the dataset. Returned distinct values will be from within the query results.


<% en.data.distinctString resultsString 'fd-regions' 'name' query %>
<% return 'resultsString' resultsString %>

<% en.data.distinctInteger resultsInteger 'accounts' 'totalEmployees' query %>
<% return 'resultsInteger' resultsInteger %>

<% en.data.distinctLong resultsLong 'accounts' '_createdAt' query %>
<% return 'resultsLong' resultsLong %>

<% en.data.distinctDouble resultsDouble 'accounts' 'totalEmployees' query %>
<% return 'resultsDouble' resultsDouble %>

<% en.data.distinctDate resultsDate 'accounts' '_created' query %>
<% return 'resultsDate' resultsDate %>
