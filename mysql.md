Set global variables:
---------------------

show global variables where Variable_name = 'long_query_time';

set global long_query_time = 40.000000;

Show grants:
------------

show grants for 'rniveau'@'%';


Find the master:
----------------

show slave status;

Find the current position of the master:
----------------------------------------

show master status

Activate slow_query_log:
------------------------

set global slow_query_log = ON;

set global long_query_time=39;

Show innodb status:
-------------------

SHOW ENGINE INNODB STATUS

Show transactions:
------------------
select trx_id, trx_mysql_thread_id, trx_started FROM information_schema.innodb_trx;

useful link: https://stackoverflow.com/questions/13148630/how-do-i-find-which-transaction-is-causing-a-waiting-for-table-metadata-lock-s

Check auto increment:
---------------------

show variables like 'auto_increment%';

Update password:
----------------

ALTER USER 'user'@'hostname' IDENTIFIED BY 'newPass';

Useful commands:
----------------

select THREAD_ID,name,PROCESSLIST_STATE,PROCESSLIST_INFO from performance_schema.threads;

show open tables where in_use>0;
