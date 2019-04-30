# Get Dataset Fields

In order get fields of a dataset, you have get the dataset. All fields will be part of that dataset.



## Get a specific dataset

<% assign datasetId = 'test1000' %>                      // Mandatory

<% en.data.sets.get results datasetId %>
<% return 'test1000-get' results %>