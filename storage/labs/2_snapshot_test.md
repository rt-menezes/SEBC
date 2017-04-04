[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -put /tmp/SEBC-master.zip /user/stailer/precious
[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -ls /user/stailer/precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     473950 2017-04-04 14:08 /user/stailer/precious/SEBC-master.zip
[hdfs@ip-10-230-82-86 ~]$ hdfs dfsadmin -allowSnapshot /user/stailer/precious
Allowing snaphot on /user/stailer/precious succeeded
[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -createSnapshot /user/stailer/precious sebc-hdfs-test
Created snapshot /user/stailer/precious/.snapshot/sebc-hdfs-test
[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -rm -r -f /user/stailer/precious
rm: Failed to move to trash: hdfs://nameservice1/user/stailer/precious: The directory /user/stailer/precious cannot be deleted since /user/stailer/precious is snapshottable and already has snapshots
[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -rm /user/stailer/precious/SEBC-master.zip
17/04/04 14:11:43 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/stailer/precious/SEBC-master.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/stailer/precious/SEBC-master.zip

# After restoring snapshot
[hdfs@ip-10-230-82-86 ~]$ hdfs dfs -ls -R /user/stailer
drwxr-xr-x   - hdfs supergroup          0 2017-04-04 14:24 /user/stailer/precious
-rw-r--r--   3 hdfs supergroup     473950 2017-04-04 14:23 /user/stailer/precious/SEBC-master.zip
