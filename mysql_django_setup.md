## Django and Mysql Setup

* connect to your MySQL database as the root\
***REMOVED*** mysql -u root -p ***REMOVED***


* create a database in MySQL run the following command \
***REMOVED*** CREATE DATABASE blog_database; ***REMOVED***

* create a separate MySQL user amar that Django will use to operate the new database (blog_database)\
***REMOVED*** CREATE USER 'amar'@'localhost' IDENTIFIED WITH mysql_native_password BY 'amar@123'; ***REMOVED***

* Grant All the user permissions to blog_database i.e: DELETE,UPDATE,CREATE etc.\
***REMOVED*** GRANT ALL ON blog_database.* TO 'amar'@'localhost'; ***REMOVED***


* Flush the privileges so that the current instance of MySQL knows about the recent changes you’ve made\
***REMOVED*** FLUSH PRIVILEGES; ***REMOVED***


* Add DATABASES setting in your django settings.py you can change your HOST(IP) accordingly where your MySql server is host for now there are using  local machine HOST.\
***REMOVED*** DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'blog_database',
            'USER': 'amar',
            'PASSWORD': 'amar@123',
            'HOST': '127.0.0.1',
            'PORT': '3306',
            'OPTIONS': {
                'init_command': "SET sql_mode='STRICT_TRANS_TABLES'",
            },
        }
    }
***REMOVED***
