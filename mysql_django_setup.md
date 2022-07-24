#connect to your MySQL database as the root\
mysql -u root -p


#create a database in MySQL run the following command \
CREATE DATABASE blog_database;

#create a separate MySQL user amar that Django will use to operate the new database (blog_database)\
CREATE USER 'amar'@'localhost' IDENTIFIED WITH mysql_native_password BY 'amar@123';

#Grant All the user permissions to blog_database i.e: DELETE,UPDATE,CREATE etc.\
GRANT ALL ON blog_database.* TO 'amar'@'localhost';


#Flush the privileges so that the current instance of MySQL knows about the recent changes you’ve made\
FLUSH PRIVILEGES;


#Add DATABASES setting in your django settings.py you can change your HOST(IP) accordingly where your MySql server is host for now there are using  local machine HOST.
DATABASES = {
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
