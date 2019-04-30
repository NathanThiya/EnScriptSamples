# Move Field up in the order
If the field moving up is the first element, it will be moved to the bottom.

```
<% assign datasetId = 'test1000' %>                      // Mandatory
<% assign fieldId = 'name' %>                      // Mandatory

<% en.data.sets.fieldMoveUp results datasetId fieldId %>
<% return 'test1000-fieldMoveUp' results %>
```