# Update dataset information


dataset id and fields cannot be updated.
Only name, description attributes can be updated.
Also additional attributes can be specified and created to maintain any other information.
The additional information will not be used by EnMobi.

```
<% assign datasetId = 'test1000' %>                      // Mandatory
<% assign dataset.name = 'Test 1000 updated' %>                  // Optional
<% assign dataset.description = 'Test 1000 dataset Updated' %>    // Optional
<% assign dataset.addionalInfo = 'Some Addional information can be stored as well' %>    // Optional
```

## Update the dataset
```
<% en.data.sets.update results datasetId dataset %>
<% return 'test1000-update' results %>
```