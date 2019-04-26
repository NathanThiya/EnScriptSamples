# Create new dataset with fields

## Define dataset object
```
<% assign dataset.id = 'test1001' %>                        // Mandatory
<% assign dataset.name = 'Test 1001' %>                     // Mandatory
<% assign dataset.description = 'Test 1001 dataset' %>      // Optional
```


## Define dataset object
```
<% assign field1.id = 'firstName' %>                        // Mandatory
<% assign field1.name = 'First Name' %>                     // Mandatory
<% assign field1.dataType = 'STRING' %>                     // Optional, default:STRING
<% assign field1.uiType = 'TEXTBOX' %>                      // Optional, default:TEXTBOX

<% assign field2.id = 'phone' %>                            // Mandatory
<% assign field2.name = 'Phone' %>                          // Mandatory
<% assign field2.dataType = 'STRING' %>                     // Optional, default:STRING
<% assign field2.uiType = 'TEXTBOX' %>                      // Optional, default:TEXTBOX

<% assign dataset.fields = [field1,field2] %>      // Optional
```
If fields available, then that will be used. Otherwise 2 default name, description fields will be created.


## Delete the dataset if exists.
```
<% en.data.sets.delete results dataset.id %>
<% return 'test1001-delete' results %>
```

## Create new dataset with default fields
```
<% en.data.sets.create results dataset %>
<% return 'test1001-create' results %>
```
