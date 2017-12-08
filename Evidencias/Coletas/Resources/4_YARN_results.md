[hdfs@ip-172-31-30-147 tmp]$ sh -x yarntest.sh
+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Thu Dec 7 19:30:06 UTC 2017
Testing loop started on Thu Dec 7 19:30:06 UTC 2017
+ for i in 8
+ for j in 1
+ for k in 512 1024
++ echo '(512*0.8)/1'
++ bc
+ MAP_MB=409
++ echo '(512*0.8)/1'
++ bc
+ RED_MB=409
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=512 -Dmapreduce.map.java.opts.max.heap=409 51200000 /tmp/tg-10GB-8-1-512

real	0m56.034s
user	0m5.607s
sys	0m0.265s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=512 -Dmapreduce.map.java.opts.max.heap=409 -Dmapreduce.reduce.memory.mb=512 -Dmapreduce.reduce.java.opts.max.heap=409 /tmp/tg-10GB-8-1-512 /tmp/ts-10GB-8-1-512

real	2m1.053s
user	0m6.787s
sys	0m0.288s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /tmp/tg-10GB-8-1-512
Deleted /tmp/tg-10GB-8-1-512
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /tmp/ts-10GB-8-1-512
Deleted /tmp/ts-10GB-8-1-512
+ for k in 512 1024
++ echo '(1024*0.8)/1'
++ bc
+ MAP_MB=819
++ echo '(1024*0.8)/1'
++ bc
+ RED_MB=819
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 51200000 /tmp/tg-10GB-8-1-1024

real	0m50.155s
user	0m5.509s
sys	0m0.251s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 -Dmapreduce.reduce.memory.mb=1024 -Dmapreduce.reduce.java.opts.max.heap=819 /tmp/tg-10GB-8-1-1024 /tmp/ts-10GB-8-1-1024

real	2m0.864s
user	0m6.642s
sys	0m0.275s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /tmp/tg-10GB-8-1-1024
Deleted /tmp/tg-10GB-8-1-1024
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /tmp/ts-10GB-8-1-1024
Deleted /tmp/ts-10GB-8-1-1024
++ date
+ echo Testing loop ended on Thu Dec 7 19:36:01 UTC 2017
Testing loop ended on Thu Dec 7 19:36:01 UTC 2017
[hdfs@ip-172-31-30-147 tmp]$ 
