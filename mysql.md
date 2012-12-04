MYSQL
=====

As user captbaritone, dump database foo to backup.sql

    mysqldump -u captbaritone -p foo > backup.sql

Same as above, but compress the output to backup.sql.gz

    mysqldump -u captbaritone -p foo | gzip > backup.sql.gz

As captbaritone, restore database foo from backup.sql

    mysql -u captbaritone -p < backup.sql

Same as above but from backup.sql.gz

    gunzip < backup.sql.gz | mysql -u captbaritone -p foo

