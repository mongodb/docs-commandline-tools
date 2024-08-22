.. warning:: Data Dump and Restore Conflicts With ($) in Collection Fields

   Starting in MongoDB 5.0, document field names can be prefixed with a
   dollar character (``$``). However, :binary:`~bin.mongoimport` and
   :binary:`~bin.mongoexport` won't work with field names that are prefixed
   with a dollar character.

   MongoDB Extended JSON v2 cannot differentiate between type wrappers and
   fields that happen to have the same name as type wrappers. Do not use
   Extended JSON formats in contexts where the corresponding BSON
   representations might include ($) prefixed keys. The DBRef mechanism is
   an exception to this general rule.
