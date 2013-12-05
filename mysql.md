MYSQL
=====

Backup/Restore
--------------

Show list of databases:

    SHOW DATABASES;

As user captbaritone, dump database foo to backup.sql

    mysqldump -u captbaritone -p foo > backup.sql

Same as above but specifying the password as 'MyPass'

    mysqldump -u captbaritone -pMyPass foo > backup.sql

Same as above, but compress the output to backup.sql.gz

    mysqldump -u captbaritone -pMyPass foo | gzip > backup.sql.gz

As captbaritone, restore database foo from backup.sql

    mysql -u captbaritone -p foo < backup.sql

As captbaritone, run the queries in update.sql on database foo

    mysql -u captbaritone -p foo < update.sql

Same as above but from backup.sql.gz

    gunzip < backup.sql.gz | mysql -u captbaritone -p foo

Access remote mysql server from commandline

    mysql -h host.example.com -u captbaritone -p database

Create
------

Create a database with a user

    # mysql -u root -p
    msyql# CRAETE DATABASE `testing`;
    mysql# GRANT ALL PRIVILEGES ON `testing`.* TO `sami-qa`@localhost IDENTIFIED BY 'my_password';

Login
-----

    mysql -u USERNAME -pPASSWORD -h HOSTNAMEORIP DATABASENAME
