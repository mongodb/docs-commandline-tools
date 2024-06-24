``mongoimport`` and ``mongoexport`` do not guarantee that documents
maintain remain in the same order during the import and export
processes. If you need to maintain document order during import and
export, use :binary:`mongodump` and :binary:`mongorestore`, which
preserve document order.
