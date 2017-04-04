time hadoop jar /opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/jars/hadoop-examples.jar teragen \
-Ddfs.blocksize=32768 \
-Ddfs.replication=1 \
-Dmapreduce.job.maps=4 \
10737418 \
/user/stailer/terasort-input > input.txt 2>&1

real	1m55.271s
user	2m9.834s
sys		0m9.321s

time hadoop jar /opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/jars/hadoop-examples.jar terasort \
/user/stailer/terasort-input \
/user/stailer/terasort-output > output.txt 2>&1

real	13m6.808s
user	15m53.695s
sys	1m26.648s
