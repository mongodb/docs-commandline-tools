When using :binary:`~bin.mongorestore` to load data files created by
:binary:`~bin.mongodump`, be sure that the deployment you are restoring 
to has either:

- The same major version.
- The same :ref:`FCV level set <set-fcv>`.

For example, if your dump was created from a MongoDB deployment running
version ``4.4.x``, be sure that the MongoDB deployment you are restoring 
to is also running version ``4.4.x`` or has the FCV level set to 
``4.4.x``.

.. note::

   The BSON files generated from ``mongodump`` are restorable 
   into MongoDB deployments starting with the version they were created 
   on and in all future versions.

   This guarantee does not apply to metadata, archive, or oplog replay 
   files.

In addition, ensure that you are using the same version of 
:binary:`~bin.mongorestore` to load the data files as the version of
:binary:`~bin.mongodump` that you used to create them. For example, if
you used :binary:`~bin.mongodump` version ``{+release+}`` to create the
dump, use :binary:`~bin.mongorestore` version ``{+release+}`` to restore
it.
