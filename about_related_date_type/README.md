# Oveview
mysql 타입 중 date, datetime, timestamp 비교

# date vs datetime vs timestamp
### 1. date
foramt : 'YYYY-MM-DD'<br>
range : '1000-01-01' to '9999-12-31'

### 2. datetime
format : 'YYYY-MM-DD hh:mm:ss'<br>
range : '1000-01-01 00:00:00' to '9999-12-31 23:59:59'

### 3. timestamp
format : 'YYYY-MM-DD hh:mm:ss'<br>
range : '1970-01-01 00:00:01' UTC to '2038-01-19 03:14:07' UTC

### 4. datetime vs timestamp
MySQL converts TIMESTAMP values from the current time zone to UTC for storage, and back from UTC to the current time zone for retrieval. (This does not occur for other types such as DATETIME.)

# Reference
* https://dev.mysql.com/doc/refman/8.0/en/datetime.html
* https://www.tech-recipes.com/rx/22599/mysql-datetime-vs-timestamp-data-type/
