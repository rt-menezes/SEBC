[root@ip-172-31-24-87 ~]# /usr/bin/mysql_secure_installation
NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MariaDB
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MariaDB to secure it, we'll need the current
password for the root user.  If you've just installed MariaDB, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none): 
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MariaDB
root user without the proper authorisation.

Set root password? [Y/n] yes
New password: 
Re-enter new password: 
Password updated successfully!
Reloading privilege tables..
 ... Success!

[root@ip-172-31-24-87 ~]# systemctl status mariadb
● mariadb.service - MariaDB database server
   Loaded: loaded (/usr/lib/systemd/system/mariadb.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2017-12-07 11:07:15 UTC; 6h ago
  Process: 909 ExecStartPost=/usr/libexec/mariadb-wait-ready $MAINPID (code=exited, status=0/SUCCESS)
  Process: 867 ExecStartPre=/usr/libexec/mariadb-prepare-db-dir %n (code=exited, status=0/SUCCESS)
 Main PID: 908 (mysqld_safe)
   CGroup: /system.slice/mariadb.service
           ├─ 908 /bin/sh /usr/bin/mysqld_safe --basedir=/usr
           └─1415 /usr/libexec/mysqld --basedir=/usr --datadir=/var/lib/mysql --plugin-dir=/usr/lib64/mysql/plugin --log-error=/var/log/mariadb/mariadb.log --pid-fil...

Dec 07 11:07:09 ip-172-31-24-87.us-east-2.compute.internal systemd[1]: Starting MariaDB database server...
Dec 07 11:07:09 ip-172-31-24-87.us-east-2.compute.internal mariadb-prepare-db-dir[867]: Database MariaDB is probably initialized in /var/lib/mysql already, noth...done.
Dec 07 11:07:09 ip-172-31-24-87.us-east-2.compute.internal mariadb-prepare-db-dir[867]: If this is not the case, make sure the /var/lib/mysql is empty before ru...-dir.
Dec 07 11:07:09 ip-172-31-24-87.us-east-2.compute.internal mysqld_safe[908]: 171207 11:07:09 mysqld_safe Logging to '/var/log/mariadb/mariadb.log'.
Dec 07 11:07:09 ip-172-31-24-87.us-east-2.compute.internal mysqld_safe[908]: 171207 11:07:09 mysqld_safe Starting mysqld daemon with databases from /var/lib/mysql
Dec 07 11:07:15 ip-172-31-24-87.us-east-2.compute.internal systemd[1]: Started MariaDB database server.
Hint: Some lines were ellipsized, use -l to show in full.


MariaDB [(none)]> show SLAVE STATUS \G
*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: ip-172-31-30-147.us-east-2.compute.internal
                  Master_User: replicador
                  Master_Port: 3306
                Connect_Retry: 10
              Master_Log_File: mysql_binary_log.000008
          Read_Master_Log_Pos: 1134842
               Relay_Log_File: mariadb-relay-bin.000002
                Relay_Log_Pos: 536
        Relay_Master_Log_File: mysql_binary_log.000007
             Slave_IO_Running: Yes
            Slave_SQL_Running: No
              Replicate_Do_DB: 
          Replicate_Ignore_DB: 
           Replicate_Do_Table: 
       Replicate_Ignore_Table: 
      Replicate_Wild_Do_Table: 
  Replicate_Wild_Ignore_Table: 
                   Last_Errno: 0
                   Last_Error: 
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 15697046
              Relay_Log_Space: 5040963
              Until_Condition: None
               Until_Log_File: 
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File: 
           Master_SSL_CA_Path: 
              Master_SSL_Cert: 
            Master_SSL_Cipher: 
               Master_SSL_Key: 
        Seconds_Behind_Master: NULL
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error: 
               Last_SQL_Errno: 0
               Last_SQL_Error: 
  Replicate_Ignore_Server_Ids: 
             Master_Server_Id: 1
