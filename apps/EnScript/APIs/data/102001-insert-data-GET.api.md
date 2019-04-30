# Insert data to a dataset

<% assign datasetId = 'test1000' %>                      // Mandatory

<% assign row.name = 'John Doe' %>
<% assign row.description = 'Some description will go here' %>


<% en.data.insert results datasetId row %>
<% return 'test1000-insert-data' results %>



## Sample Row inserted
"row": {
    "name": "John Doe",
    "description": "Some description will go here",
    
     When a row is created below fields are automatically created for each record
    
    A Unique identified, this will always be unique in EnMobi eco system.
    "_id": "mzis3jxta0-4e01a562-3767-4398-b5cb-3e092d6c55c0",
    
    Updated time stored as long data type - This is deprecated, don't use.
    "_updatedAt": 1554357839432,
    
    Updated time stored as date/time data type - This is what should be used
    "_updated": 1554357839432,
    "_updated_": "2019-04-04T06:03:59.432Z", // This attribute is not stored. only a string representation of previous date attribute.
    
    User id of who updated it. This could be null if guest user inserted the data.
    "_updatedBy": "zqot149exz-2d2e331a-11cc-4763-ae2b-6eadb3061e57",
    
    Created time stored as long data type - This is deprecated, don't use.
    "_createdAt": 1554357839432,
    
    Created time stored as date/time data type - This is what should be used
    "_created": 1554357839432,
    "_created_": "2019-04-04T06:03:59.432Z", // This attribute is not stored. only a string representation of previous date attribute.
    
    User id of who created it. This could be null if guest user inserted the data.
    "_createdBy": "zqot149exz-2d2e331a-11cc-4763-ae2b-6eadb3061e57",
    
    When was the last time this record was updated
    "_t": 1554357839432
}