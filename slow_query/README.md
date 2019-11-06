# Overview
How to analyze slow query


# Enable slow query log
By default, the slow query log is disabled.
```bash
mysql> SET GLOBAL slow_query_log = 1;
mysql> SET GLOBAL long_query_time = 5;
mysql> SET GLOBAL log_queries_not_using_indexes = 1;
mysql> show global variables like '%quer%';
+----------------------------------------+--------------------------------------+
| Variable_name                          | Value                                |
+----------------------------------------+--------------------------------------+
| binlog_rows_query_log_events           | OFF                                  |
| ft_query_expansion_limit               | 20                                   |
| have_query_cache                       | YES                                  |
| log_queries_not_using_indexes          | ON                                   |
| log_throttle_queries_not_using_indexes | 0                                    |
| long_query_time                        | 5.000000                             |
| query_alloc_block_size                 | 8192                                 |
| query_cache_limit                      | 1048576                              |
| query_cache_min_res_unit               | 4096                                 |
| query_cache_size                       | 16777216                             |
| query_cache_type                       | OFF                                  |
| query_cache_wlock_invalidate           | OFF                                  |
| query_prealloc_size                    | 8192                                 |
| slow_query_log                         | ON                                   |
| slow_query_log_file                    | /var/lib/mysql/203ba254ed70-slow.log |
+----------------------------------------+--------------------------------------+
```


# Analyz slow queries
```bash
mysql> SELECT SLEEP(11);
mysql> SELECT SLEEP(11);
# mysqldumpslow
Reading mysql slow query log from /var/lib/mysql/203ba254ed70-slow.log
Count: 2  Time=11.00s (22s)  Lock=0.00s (0s)  Rows=1.0 (2), root[root]@localhost
  select sleep(N)
```





# Reference
* https://dev.mysql.com/doc/refman/5.7/en/slow-query-log.html
* https://dev.mysql.com/doc/refman/5.7/en/mysqldumpslow.html
* https://blog.toadworld.com/2017/08/09/logging-and-analyzing-slow-queries-in-mysql
