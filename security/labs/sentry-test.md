```
beeline> !connect jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
scan complete in 3ms
Connecting to jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-146-179-98.ec2.internal> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170406000000_bb66e518-ebd5-4652-a642-a2f57f41e568): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170406000000_bb66e518-ebd5-4652-a642-a2f57f41e568); Time taken: 0.646 seconds
INFO  : Executing command(queryId=hive_20170406000000_bb66e518-ebd5-4652-a642-a2f57f41e568): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170406000000_bb66e518-ebd5-4652-a642-a2f57f41e568); Time taken: 0.249 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.23 seconds)
0: jdbc:hive2://ip-10-146-179-98.
```

#george should be able to see all tables
```
[root@ip-10-146-179-98 ~]# su - george
[george@ip-10-146-179-98 ~]$ kinit
Password for george@CLOUDERA: 
[george@ip-10-146-179-98 ~]$ beeline 
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
scan complete in 2ms
Connecting to jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-146-179-98.ec2.internal> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170406001414_a4d00b78-c63c-493a-ae8c-a2ddf40d8b6f): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170406001414_a4d00b78-c63c-493a-ae8c-a2ddf40d8b6f); Time taken: 0.06 seconds
INFO  : Executing command(queryId=hive_20170406001414_a4d00b78-c63c-493a-ae8c-a2ddf40d8b6f): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170406001414_a4d00b78-c63c-493a-ae8c-a2ddf40d8b6f); Time taken: 0.147 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.326 seconds)
```

#ferdinand should see sample_07
```
[root@ip-10-146-179-98 ~]# su - ferdinand
[ferdinand@ip-10-146-179-98 ~]$ kinit
Password for ferdinand@CLOUDERA: 
[ferdinand@ip-10-146-179-98 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1200
Default principal: ferdinand@CLOUDERA

Valid starting       Expires              Service principal
04/06/2017 00:16:18  04/07/2017 00:16:18  krbtgt/CLOUDERA@CLOUDERA
	renew until 04/13/2017 00:16:18
[ferdinand@ip-10-146-179-98 ~]$ beeline 
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
scan complete in 2ms
Connecting to jdbc:hive2://ip-10-146-179-98.ec2.internal:10000/default;principal=hive/ip-10-146-179-98.ec2.internal@CLOUDERA
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-146-179-98.ec2.internal> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170406001616_b4bd1a2a-9d98-49a4-aa43-133714b3628a): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170406001616_b4bd1a2a-9d98-49a4-aa43-133714b3628a); Time taken: 0.062 seconds
INFO  : Executing command(queryId=hive_20170406001616_b4bd1a2a-9d98-49a4-aa43-133714b3628a): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170406001616_b4bd1a2a-9d98-49a4-aa43-133714b3628a); Time taken: 0.128 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.289 seconds)
0: jdbc:hive2://ip-10-146-179-9
```