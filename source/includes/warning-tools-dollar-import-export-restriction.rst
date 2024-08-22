Starting in MongoDB 5.0, document field names can be prefixed with a
dollar character (``$``). However, :binary:`~bin.mongoimport` and
:binary:`~bin.mongoexport` won't work with field names that use the
dollar character.
