:binary:`~bin.mongoimport` and :binary:`~bin.mongoexport` are not
intended for the following use cases:

- backing up and restoring data
- sending data from a MongoDB instance to another instance and then back
  to the original instance

Instead, use :binary:`~bin.mongodump` or :binary:`~bin.mongorestore`. 