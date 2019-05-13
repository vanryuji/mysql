# Overview
InnoDB vs MyISAM

# Environment
* MySQL 8.0

# InnoDB vs MyISAM
![alt text](innodb_vs_myisam.png)<br>
* Clustered indexes<br>
    * Clustered index란? : Primary Key와 같은 개념<br>
    * Join performance : InnoDB에는 Clustered index / Foriegn key가 존재하기에 join에서는 당연히 성능 좋음, 하지만 MyISAM에서는 Clustered index를 지원하지 않기에 join에서 성능이 별로<br>
* Transactions<br>
    * Commit and Rollback for MyISAM : auto-commit만 지원하고 commit/rollback은 무시<br>

# Choosing a storage engine
* InnoDB : It is an engine that performs well and offers many of required attributes that any database would need
* MyISAM : Read-heavy application

# Reference
* https://dev.mysql.com/doc/refman/8.0/en/storage-engines.html
* https://dev.mysql.com/doc/refman/8.0/en/glossary.html#glos_clustered_index
* https://www.percona.com/blog/2006/05/29/join-performance-of-myisam-and-innodb/
* https://stackoverflow.com/questions/8036005/myisam-engine-transaction-support
