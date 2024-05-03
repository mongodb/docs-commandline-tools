When using :binary:`~bin.mongorestore` to load data files created by
:binary:`~bin.mongodump`, the MongoDB versions of your source and 
destination deployments must be either:

- The same major version.
- The same feature compatibility version. 

For example, if your dump was created from a MongoDB deployment running
version ``4.4``, the MongoDB deployment you restore to must also run 
version ``4.4`` or have its FCV set to ``4.4``.

To change your feature compatibility version, see 
:dbcommand:`setFeatureCompatibilityVersion`.

.. note::

   You can restore the BSON files generated from ``mongodump`` into
   MongoDB deployments running the same version or one major version
   later than the source deployment. For example, to restore to a
   MongoDB {+server-version+} deployment from a source deployment that
   is lower than MongoDB {+server-previous-version+}, you must
   successively upgrade the major release of the source deployment until
   you upgrade to {+server-previous-version+}-series. To learn how to
   upgrade your deployment, see the :manual:`upgrade documentation
   </release-notes/{+server-version+}-upgrade>`.

   This guarantee does not apply to metadata, archive, or oplog replay 
   files. If you try to restore these files using different 
   source and destination deployment versions, the ``mongorestore`` 
   process could result in failure, silent failure, or corrupted 
   metadata.

In addition, ensure that you are using the same version of 
:binary:`~bin.mongorestore` to load the data files as the version of
:binary:`~bin.mongodump` that you used to create them. For example, if
you used :binary:`~bin.mongodump` version ``{+release+}`` to create the
dump, use :binary:`~bin.mongorestore` version ``{+release+}`` to restore
it.
