## Importing a Database
``` 
mysql -u root -p database_name < ~/path-of-Sql-file/data-dump.sql 
``` 
Note that you need to change the database_name with the actual name of your database and the username part with your existing MySQL username like root, amar_user etc.
* If you are same dir there data-dump.sql do not use ~/

## Exporting a Database
```
mysqldump -u username -p database_name > data-dump.sql 
```
Note that you need to change the database_name with the actual name of your database and the username part with your existing MySQL username like root, amar_user etc.
* You can change data-dump.sql filename there you will export all database.


