The :term:`oplog` contains the history of database write operations.

To create a consistent ``mongodump`` backup file using :term:`oplog`
entries, use the :option:`mongodump --oplog` option. To restore data
from the backup file, use the :option:`mongorestore --oplogReplay`
option.

``mongodump`` outputs:

- Collection documents, metadata, and options.
- Index definitions.
- Writes that occur during the ``mongodump`` run, if run with the
  ``mongodump --oplog`` option.

Use mongodump with the oplog Option
```````````````````````````````````

The ``mongodump --oplog`` option creates a file named :file:`oplog.bson`
in the top level of the ``mongodump`` output directory. The file
contains write operations that occur during the ``mongodump`` run.
Writes that occur after ``mongodump`` completes aren't recorded in the
``oplog.bson`` file for that ``mongodump`` run.

To back up sharded clusters with ``mongodump``, see
:ref:`backup-sharded-dumps`.

Use mongorestore with the oplogReplay Option
````````````````````````````````````````````

To restore oplog entries from the ``oplog.bson`` file, use the
``mongorestore --oplogReplay`` option. Use ``mongodump --oplog``
together with ``mongorestore --oplogReplay`` to ensure the database is
current and has all writes that occurred during the ``mongodump`` run.

Other Backup and Restore Methods
````````````````````````````````

For other migration and backup methods, see:

- :atlas:`Migrate or import data </import>` in Atlas.
- :atlas:`Back up, restore, and archive data </backup-restore-cluster>`
  in Atlas.
- `mongosync
  <https://www.mongodb.com/docs/cluster-to-cluster-sync/current/reference/mongosync>`__
  utility.
