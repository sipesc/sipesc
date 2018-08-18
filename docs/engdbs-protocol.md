Database communication protocol
===============================

Error Reponse
-------------
 - ErrorCode (>0)
 - ErrorMessage (String)

List Server Root
----------------
 * Request:
   - ListRootRequestCode (0)
   - ArgumentCount (0)
 * Response:
   - SuccessCode (0)
   - DatabaseCount (>=0)
   - DatabaseName (DatabaseCount times)

Open Database
-------------
 * Request:
   - OpenDatabaseRequestCode (1)
   - ArgumentCount (1)
   - DatabaseName (String)
 * Response:
   - SuccessCode (0)
   - Count (1)
   - DatabaseId (>=0)

List Database
-------------
 * Request:
   - ListDatabaseRequestCode (2)
   - ArgumentCount (1)
   - DatabaseId (>=0)
 * Response:
   - SuccessCode (0)
   - ItemCount (>=0)
   - ItemName (ItemCount times)

Close Database
--------------
 * Request:
   - CloseDatabaseRequestCode (3)
   - ArgumentCount (1)
   - DatabaseId (>=0)
 * Response:
   - SuccessCode (0)
   - Count (0)

Remove Database
---------------
 * Request:
   - RemoveDatabaseRequestCode (4)
   - ArgumentCount (1)
   - DatabaseId (>=0)
 * Response:
   - SuccessCode (0)
   - Count (0)

