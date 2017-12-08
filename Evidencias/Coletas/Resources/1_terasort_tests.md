[hdfs@ip-172-31-30-147 ~]$ time hadoop jar /opt/cloudera/parcels/CDH-5.12.1-1.cdh5.12.1.p0.3/jars/hadoop-examples.jar terasort /input /output
17/12/07 20:01:11 INFO terasort.TeraSort: starting
17/12/07 20:01:12 INFO input.FileInputFormat: Total input paths to process : 2
Spent 102ms computing base-splits.
Spent 2ms computing TeraScheduler splits.
Computing input splits took 105ms
Sampling 2 splits of 2
Making 6 from 100000 sampled records
Computing parititions took 395ms
Spent 502ms computing partitions.
17/12/07 20:01:13 INFO mapreduce.JobSubmitter: number of splits:2
17/12/07 20:01:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512669756012_0013
17/12/07 20:01:13 INFO impl.YarnClientImpl: Submitted application application_1512669756012_0013
17/12/07 20:01:13 INFO mapreduce.Job: The url to track the job: http://ip-172-31-24-87.us-east-2.compute.internal:8088/proxy/application_1512669756012_0013/
17/12/07 20:01:13 INFO mapreduce.Job: Running job: job_1512669756012_0013
17/12/07 20:01:18 INFO mapreduce.Job: Job job_1512669756012_0013 running in uber mode : false
17/12/07 20:01:18 INFO mapreduce.Job:  map 0% reduce 0%
17/12/07 20:01:24 INFO mapreduce.Job:  map 100% reduce 0%
17/12/07 20:01:30 INFO mapreduce.Job:  map 100% reduce 33%
17/12/07 20:01:31 INFO mapreduce.Job:  map 100% reduce 100%
17/12/07 20:01:32 INFO mapreduce.Job: Job job_1512669756012_0013 completed successfully
17/12/07 20:01:32 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=44352937
		FILE: Number of bytes written=89941583
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=102400202
		HDFS: Number of bytes written=102400000
		HDFS: Number of read operations=24
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters 
		Launched map tasks=2
		Launched reduce tasks=6
		Data-local map tasks=1
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=7803
		Total time spent by all reduces in occupied slots (ms)=22557
		Total time spent by all map tasks (ms)=7803
		Total time spent by all reduce tasks (ms)=22557
		Total vcore-milliseconds taken by all map tasks=7803
		Total vcore-milliseconds taken by all reduce tasks=22557
		Total megabyte-milliseconds taken by all map tasks=7990272
		Total megabyte-milliseconds taken by all reduce tasks=23098368
	Map-Reduce Framework
		Map input records=1024000
		Map output records=1024000
		Map output bytes=104448000
		Map output materialized bytes=44368702
		Input split bytes=202
		Combine input records=0
		Combine output records=0
		Reduce input groups=1024000
		Reduce shuffle bytes=44368702
		Reduce input records=1024000
		Reduce output records=1024000
		Spilled Records=2048000
		Shuffled Maps =12
		Failed Shuffles=0
		Merged Map outputs=12
		GC time elapsed (ms)=644
		CPU time spent (ms)=15940
		Physical memory (bytes) snapshot=2585100288
		Virtual memory (bytes) snapshot=22413561856
		Total committed heap usage (bytes)=2824339456
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=102400000
	File Output Format Counters 
		Bytes Written=102400000
17/12/07 20:01:32 INFO terasort.TeraSort: done

real	0m22.156s
user	0m6.212s
sys	0m0.268s
[hdfs@ip-172-31-30-147 ~]$ 
