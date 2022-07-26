## Importing a Database
***REMOVED*** 
mysql -u root -p databasename < ~/path-of-Sql-file/data-dump.sql 
***REMOVED*** 
Note that you need to change the database_name with the actual name of your database and the username part with your existing MySQL username like root, amar_user.

*if you are same dir there data-dump.sql do not use ~/

## Exporting a Database
***REMOVED***
mysqldump -u username -p database_name > data-dump.sql 
***REMOVED***

Note that you need to change the database_name with the actual name of your database and the username part with your existing MySQL username like root, amar_user.
and can change data-dump.sql filename there you will export all database


