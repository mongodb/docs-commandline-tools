:binary:`~bin.mongoimport` in conjunction with
:binary:`~bin.mongoexport` is not a recommended method for the
following use cases:

- backing up and restoring data
- transforming data from one format to another and then back to the
  original format

For these cases, use :binary:`~bin.mongodump` or
:binary:`~bin.mongorestore`. 