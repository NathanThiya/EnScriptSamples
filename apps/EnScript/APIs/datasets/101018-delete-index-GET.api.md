# Delete a specific index on a dataset

en.data.sets.deleteIndex datasetId indexName



# Delete all indexes on a dataset

en.data.sets.deleteAllIndexes datasetId


<% assign datasetId     = 'accounts' %>

<% en.data.sets.deleteAllIndexes results datasetId %>

<% return 'results' results  %>
