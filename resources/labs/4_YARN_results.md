+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Tue Apr 4 19:16:40 UTC 2017
Testing loop started on Tue Apr 4 19:16:40 UTC 2017
+ for i in 8
+ for j in 1
+ for k in 512 1024
++ echo '(512*0.8)/1'
++ bc
+ MAP_MB=409
++ echo '(512*0.8)/1'
++ bc
+ RED_MB=409
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=512 -Dmapreduce.map.java.opts.max.heap=409 51200000 /results/tg-10GB-8-1-512

real	0m58.578s
user	1m5.225s
sys	0m4.869s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=512 -Dmapreduce.map.java.opts.max.heap=409 -Dmapreduce.reduce.memory.mb=512 -Dmapreduce.reduce.java.opts.max.heap=409 /results/tg-10GB-8-1-512 /results/ts-10GB-8-1-512

real	7m19.734s
user	6m21.422s
sys	0m43.828s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-8-1-512
Deleted /results/tg-10GB-8-1-512
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-8-1-512
Deleted /results/ts-10GB-8-1-512
+ for k in 512 1024
++ echo '(1024*0.8)/1'
++ bc
+ MAP_MB=819
++ echo '(1024*0.8)/1'
++ bc
+ RED_MB=819
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 51200000 /results/tg-10GB-8-1-1024

real	1m15.403s
user	1m5.176s
sys	0m4.809s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 -Dmapreduce.reduce.memory.mb=1024 -Dmapreduce.reduce.java.opts.max.heap=819 /results/tg-10GB-8-1-1024 /results/ts-10GB-8-1-1024

real	7m17.860s
user	6m30.800s
sys	0m47.043s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-8-1-1024
Deleted /results/tg-10GB-8-1-1024
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-8-1-1024
Deleted /results/ts-10GB-8-1-1024
++ date
+ echo Testing loop ended on Tue Apr 4 19:33:43 UTC 2017
Testing loop ended on Tue Apr 4 19:33:43 UTC 2017




+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Tue Apr 4 19:38:06 UTC 2017
Testing loop started on Tue Apr 4 19:38:06 UTC 2017
+ for i in 16
+ for j in 8
+ for k in 2048 4096
++ echo '(2048*0.8)/1'
++ bc
+ MAP_MB=1638
++ echo '(2048*0.8)/1'
++ bc
+ RED_MB=1638
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=16 -Dmapreduce.map.memory.mb=2048 -Dmapreduce.map.java.opts.max.heap=1638 51200000 /results/tg-10GB-16-8-2048

real	0m58.315s
user	1m4.888s
sys	0m4.417s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=16 -Dmapreduce.job.reduces=8 -Dmapreduce.map.memory.mb=2048 -Dmapreduce.map.java.opts.max.heap=1638 -Dmapreduce.reduce.memory.mb=2048 -Dmapreduce.reduce.java.opts.max.heap=1638 /results/tg-10GB-16-8-2048 /results/ts-10GB-16-8-2048

real	6m1.576s
user	5m58.228s
sys	0m38.320s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-16-8-2048
Deleted /results/tg-10GB-16-8-2048
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-16-8-2048
Deleted /results/ts-10GB-16-8-2048
+ for k in 2048 4096
++ echo '(4096*0.8)/1'
++ bc
+ MAP_MB=3276
++ echo '(4096*0.8)/1'
++ bc
+ RED_MB=3276
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=16 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 51200000 /results/tg-10GB-16-8-4096

real	1m12.235s
user	1m6.080s
sys	0m4.645s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=16 -Dmapreduce.job.reduces=8 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 -Dmapreduce.reduce.memory.mb=4096 -Dmapreduce.reduce.java.opts.max.heap=3276 /results/tg-10GB-16-8-4096 /results/ts-10GB-16-8-4096

real	5m58.703s
user	6m1.040s
sys	0m38.406s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-16-8-4096
Deleted /results/tg-10GB-16-8-4096
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-16-8-4096
Deleted /results/ts-10GB-16-8-4096
++ date
+ echo Testing loop ended on Tue Apr 4 19:52:29 UTC 2017
Testing loop ended on Tue Apr 4 19:52:29 UTC 2017


+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Tue Apr 4 23:09:43 UTC 2017
Testing loop started on Tue Apr 4 23:09:43 UTC 2017
+ for i in 8
+ for j in 4
+ for k in 4096 8192
++ echo '(4096*0.8)/1'
++ bc
+ MAP_MB=3276
++ echo '(4096*0.8)/1'
++ bc
+ RED_MB=3276
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 51200000 /results/tg-10GB-8-4-4096

real	0m59.322s
user	1m5.831s
sys	0m4.621s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=4 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 -Dmapreduce.reduce.memory.mb=4096 -Dmapreduce.reduce.java.opts.max.heap=3276 /results/tg-10GB-8-4-4096 /results/ts-10GB-8-4-4096

real	6m14.507s
user	6m11.833s
sys	0m39.623s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-8-4-4096
Deleted /results/tg-10GB-8-4-4096
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-8-4-4096
Deleted /results/ts-10GB-8-4-4096
+ for k in 4096 8192
++ echo '(8192*0.8)/1'
++ bc
+ MAP_MB=6553
++ echo '(8192*0.8)/1'
++ bc
+ RED_MB=6553
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=8 -Dmapreduce.map.memory.mb=8192 -Dmapreduce.map.java.opts.max.heap=6553 51200000 /results/tg-10GB-8-4-8192

real	0m59.189s
user	1m4.665s
sys	0m4.389s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=8 -Dmapreduce.job.reduces=4 -Dmapreduce.map.memory.mb=8192 -Dmapreduce.map.java.opts.max.heap=6553 -Dmapreduce.reduce.memory.mb=8192 -Dmapreduce.reduce.java.opts.max.heap=6553 /results/tg-10GB-8-4-8192 /results/ts-10GB-8-4-8192

real	6m14.548s
user	6m9.016s
sys	0m41.840s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-8-4-8192
Deleted /results/tg-10GB-8-4-8192
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-8-4-8192
Deleted /results/ts-10GB-8-4-8192
++ date
+ echo Testing loop ended on Tue Apr 4 23:24:22 UTC 2017
Testing loop ended on Tue Apr 4 23:24:22 UTC 2017


+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Tue Apr 4 23:25:27 UTC 2017
Testing loop started on Tue Apr 4 23:25:27 UTC 2017
+ for i in 3
+ for j in 1
+ for k in 1024 4096
++ echo '(1024*0.8)/1'
++ bc
+ MAP_MB=819
++ echo '(1024*0.8)/1'
++ bc
+ RED_MB=819
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=3 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 51200000 /results/tg-10GB-3-1-1024

real	1m2.115s
user	1m5.589s
sys	0m4.612s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=3 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 -Dmapreduce.reduce.memory.mb=1024 -Dmapreduce.reduce.java.opts.max.heap=819 /results/tg-10GB-3-1-1024 /results/ts-10GB-3-1-1024

real	7m23.403s
user	6m17.603s
sys	0m44.864s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-3-1-1024
Deleted /results/tg-10GB-3-1-1024
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-3-1-1024
Deleted /results/ts-10GB-3-1-1024
+ for k in 1024 4096
++ echo '(4096*0.8)/1'
++ bc
+ MAP_MB=3276
++ echo '(4096*0.8)/1'
++ bc
+ RED_MB=3276
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=3 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 51200000 /results/tg-10GB-3-1-4096

real	1m1.997s
user	1m6.684s
sys	0m4.913s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=3 -Dmapreduce.job.reduces=1 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 -Dmapreduce.reduce.memory.mb=4096 -Dmapreduce.reduce.java.opts.max.heap=3276 /results/tg-10GB-3-1-4096 /results/ts-10GB-3-1-4096

real	7m9.619s
user	6m19.611s
sys	0m45.044s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-3-1-4096
Deleted /results/tg-10GB-3-1-4096
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-3-1-4096
Deleted /results/ts-10GB-3-1-4096
++ date
+ echo Testing loop ended on Tue Apr 4 23:42:16 UTC 2017
Testing loop ended on Tue Apr 4 23:42:16 UTC 2017


+ MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
+ HADOOP=/opt/cloudera/parcels/CDH/bin
++ date
+ echo Testing loop started on Tue Apr 4 23:46:59 UTC 2017
Testing loop started on Tue Apr 4 23:46:59 UTC 2017
+ for i in 12
+ for j in 3
+ for k in 1024 4096
++ echo '(1024*0.8)/1'
++ bc
+ MAP_MB=819
++ echo '(1024*0.8)/1'
++ bc
+ RED_MB=819
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=12 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 51200000 /results/tg-10GB-12-3-1024

real	1m0.563s
user	1m6.981s
sys	0m4.778s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=12 -Dmapreduce.job.reduces=3 -Dmapreduce.map.memory.mb=1024 -Dmapreduce.map.java.opts.max.heap=819 -Dmapreduce.reduce.memory.mb=1024 -Dmapreduce.reduce.java.opts.max.heap=819 /results/tg-10GB-12-3-1024 /results/ts-10GB-12-3-1024

real	4m4.843s
user	4m5.646s
sys	0m25.002s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-12-3-1024
Deleted /results/tg-10GB-12-3-1024
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-12-3-1024
Deleted /results/ts-10GB-12-3-1024
+ for k in 1024 4096
++ echo '(4096*0.8)/1'
++ bc
+ MAP_MB=3276
++ echo '(4096*0.8)/1'
++ bc
+ RED_MB=3276
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=12 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 51200000 /results/tg-10GB-12-3-4096

real	0m59.429s
user	1m5.578s
sys	0m4.744s
+ /opt/cloudera/parcels/CDH/bin/hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapreduce.job.maps=12 -Dmapreduce.job.reduces=3 -Dmapreduce.map.memory.mb=4096 -Dmapreduce.map.java.opts.max.heap=3276 -Dmapreduce.reduce.memory.mb=4096 -Dmapreduce.reduce.java.opts.max.heap=3276 /results/tg-10GB-12-3-4096 /results/ts-10GB-12-3-4096

real	5m28.614s
user	5m19.657s
sys	0m35.195s
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/tg-10GB-12-3-4096
Deleted /results/tg-10GB-12-3-4096
+ /opt/cloudera/parcels/CDH/bin/hadoop fs -rm -r -skipTrash /results/ts-10GB-12-3-4096
Deleted /results/ts-10GB-12-3-4096
++ date
+ echo Testing loop ended on Tue Apr 4 23:58:44 UTC 2017
Testing loop ended on Tue Apr 4 23:58:44 UTC 2017
