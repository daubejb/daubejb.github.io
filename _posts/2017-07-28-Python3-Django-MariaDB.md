[sudo] password for jedaube: 
Installing MariaDB/MySQL system tables in '/var/lib/mysql' ...
2017-07-28 16:19:05 140550176287040 [Note] /usr/libexec/mysqld (mysqld 10.1.25-MariaDB) starting as process 23068 ...
OK
Filling help tables...
2017-07-28 16:19:08 139953452984640 [Note] /usr/libexec/mysqld (mysqld 10.1.25-MariaDB) starting as process 23099 ...
OK
Creating OpenGIS required SP-s...
2017-07-28 16:19:11 139752311392576 [Note] /usr/libexec/mysqld (mysqld 10.1.25-MariaDB) starting as process 23132 ...
OK

To start mysqld at boot time you have to copy
support-files/mysql.server to the right place for your system

PLEASE REMEMBER TO SET A PASSWORD FOR THE MariaDB root USER !
To do so, start the server, then issue the following commands:

'/usr/bin/mysqladmin' -u root password 'new-password'
'/usr/bin/mysqladmin' -u root -h work password 'new-password'

Alternatively you can run:
'/usr/bin/mysql_secure_installation'

which will also give you the option of removing the test
databases and anonymous user created by default.  This is
strongly recommended for production servers.

See the MariaDB Knowledgebase at http://mariadb.com/kb or the
MySQL manual for more instructions.

You can start the MariaDB daemon with:
cd '/usr' ; /usr/bin/mysqld_safe --datadir='/var/lib/mysql'

You can test the MariaDB daemon with mysql-test-run.pl
cd '/usr/mysql-test' ; perl mysql-test-run.pl

Please report any problems at http://mariadb.org/jira

The latest information about MariaDB is available at http://mariadb.org/.
You can find additional information about the MySQL part at:
http://dev.mysql.com
Consider joining MariaDB's strong and vibrant community:
https://mariadb.org/get-involved/
