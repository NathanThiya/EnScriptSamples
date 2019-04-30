# Export data to CSV file

Only field dataTypes that are STRING, INTEGER, DOUBLE, DATE fields can be exported.
Fields that are being exported must be defined in the dataset.
This API will launch save as file dialog.
This API should be called as the last API call.
Any code after this API will not be able execute properly.

Param           | Description
----------------|------------
datasetId       | Dataset Id
query           | Query Object
fieldsString    | Comma separated list of field ids to be exported. The exported file field order will be maintained.
                | Each field that should be exported must be defined at the dataset level.


```
<% assign datasetId = 'contacts' %>         // Mandatory
<% assign exportFields = 'email,firstName,lastName' %>      // Mandatory

<% en.data.sets.exportToCSV results datasetId query exportFields %>
<% return 'results' results %>
```