mysql -u root -p

CREATE DATABASE blog_database;


CREATE USER 'amar'@'localhost' IDENTIFIED WITH mysql_native_password BY 'amar@123';


GRANT ALL ON blog_database.* TO 'amar'@'localhost';

FLUSH PRIVILEGES;



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
