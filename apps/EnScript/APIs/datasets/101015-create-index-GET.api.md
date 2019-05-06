# Create Index


en.data.sets.createIndex results datasetId name fields unique sparse collation.



Name        | Description
------------|-------------
datasetId   | id or _id of a dataset
name        | name of the index. Name has to be unique within a dataset
fields      | Fields to be indexed. The order in which they are specified should match to the query, so that the query can make use of the index.
            | 
unique      | Unique will enforce the uniqueness of the value within the dataset.
sparse      | Sparse will only index the documents that has the indexed attribute
collation   | Collation is an Object. Collation helps to index based on other locales. The only attribute supported is locale

<% assign datasetId     = 'accounts' %>
<% assign name          = 'accounts-name-idx' %> // name of the index
<% assign fields.name   = 1 %> // 1 - Ascending, -1 Decending
<% assign unique        = false %>
<% assign sparse        = false %>

<% en.data.sets.createIndex results datasetId name fields unique sparse %>
<% return 'results' results  %>


<% assign name                   = 'accounts-annualrevenue-idx' %> // name of the index
<% assign fields.annualRevenue   = -1 %> // 1 - Ascending, -1 Decending

<% en.data.sets.createIndex results2 datasetId name fields unique sparse %>
<% return 'results2' results2  %>


