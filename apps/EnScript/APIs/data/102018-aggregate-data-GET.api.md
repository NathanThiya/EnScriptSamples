# Aggregate query on a datset

This API allows to perform MongoDBs aggregate query.
Refer to [MongoDB Aggregate Query](https://docs.mongodb.com/manual/reference/method/db.collection.aggregate/)

en.data.aggregate results datasetId stages

Name        | Description
------------|-------------
results     | This APIs results will be returned here.
datasetId   | id or _id of dataset 
stages      | stages is an array of multiple aggregate stages. Refer to MongoDB documentation for more details.


Some of stages may require addional indexes on the fields. Without the indexes, aggregate query may fail.


