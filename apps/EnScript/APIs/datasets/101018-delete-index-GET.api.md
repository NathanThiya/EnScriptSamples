# Delete a specific index on a dataset

en.data.sets.deleteIndex datasetId indexName

<% assign datasetId     = 'accounts' %>
<% assign indexName     = 'accounts-name-idx' %>

<% en.data.sets.deleteIndex results datasetId indexName %>

<% return 'results' results  %>

# Delete all indexes on a dataset
en.data.sets.deleteAllIndexes datasetId


<% en.data.sets.deleteAllIndexes results2 datasetId %>

<% return 'results2' results2  %>

en.data.sets.deleteIndex datasetId indexName