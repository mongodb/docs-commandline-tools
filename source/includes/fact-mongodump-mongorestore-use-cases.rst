:binary:`~bin.mongoimport` and :binary:`~bin.mongoexport` are not
intended for the following use cases:

- backing up and restoring data
- converting data to a different format and then back to the original
  format
- sending data to a new destination and then back to the source

Instead, use :binary:`~bin.mongodump` or :binary:`~bin.mongorestore`. 