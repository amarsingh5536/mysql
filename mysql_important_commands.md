#export an SQL file using the command line in MySQL\
mysql -u root -p apos_test < ~/path-of-dotSql-file/data-dump.sql #if you are same dir there data-dump.sql do not use ~/

#import an SQL file using the command line in MySQL\
mysqldump -u username -p database_name > data-dump.sql


