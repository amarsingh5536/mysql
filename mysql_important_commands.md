## Exporting a Database
#export an SQL file using the command line in MySQL\
***REMOVED*** 
mysql -u root -p databasename < ~/path-of-dotSql-file/data-dump.sql 
***REMOVED*** 
Note that you need to change the database_name with the actual name of your database and the `your_username` part with your existing MySQL username(root).

*if you are same dir there data-dump.sql do not use ~/

## Importing a Database
***REMOVED***
mysqldump -u username -p database_name > data-dump.sql 
***REMOVED***

Note that you need to change the database_name with the actual name of your database and the `your_username` part with your existing MySQL username(root).
and can change data-dump.sql filename there you will import all data


