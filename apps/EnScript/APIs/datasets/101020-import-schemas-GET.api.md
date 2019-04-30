# Import Schemas


## en.data.sets.importSchemas results 



This API works with file upload. So create a POST or PUT API and include this API call to import dataset schemas.

Note: Currently this API only supports single file at a time. Each upload should only contain 1 *.enschema file.
When exporting the schemas downloaded as a ZIP file. Extract the ZIP file to find *.enschema file.

While importing a schema if the dataset already exists in current workspace, the following will happen:
Any additional fields in the importing schema will be added to the current dataset existing in workspace.
If the current dataset has any extra fields, those fields will stay untouched. 

