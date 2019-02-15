# Teragen

[centos@ip-172-31-34-255 ~]$ sudo -u zdenekapt  hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.block.size=32000000 -Dmapred.map.tasks=4 100000000 /user/zdenekapt/10-gb-file
19/02/14 10:21:13 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-255.eu-central-1.compute.internal/172.31.34.255:8032
19/02/14 10:21:14 INFO terasort.TeraGen: Generating 100000000 using 4
19/02/14 10:21:14 INFO mapreduce.JobSubmitter: number of splits:4
19/02/14 10:21:14 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/02/14 10:21:14 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
19/02/14 10:21:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1550131648250_0002
19/02/14 10:21:14 INFO impl.YarnClientImpl: Submitted application application_1550131648250_0002
19/02/14 10:21:14 INFO mapreduce.Job: The url to track the job: http://ip-172-31-34-255.eu-central-1.compute.internal:8088/proxy/application_1550131648250_0002/
19/02/14 10:21:14 INFO mapreduce.Job: Running job: job_1550131648250_0002
19/02/14 10:21:19 INFO mapreduce.Job: Job job_1550131648250_0002 running in uber mode : false
19/02/14 10:21:19 INFO mapreduce.Job:  map 0% reduce 0%
19/02/14 10:21:36 INFO mapreduce.Job:  map 43% reduce 0%
19/02/14 10:21:42 INFO mapreduce.Job:  map 67% reduce 0%
19/02/14 10:21:47 INFO mapreduce.Job:  map 70% reduce 0%
19/02/14 10:21:48 INFO mapreduce.Job:  map 78% reduce 0%
19/02/14 10:21:53 INFO mapreduce.Job:  map 80% reduce 0%
19/02/14 10:21:54 INFO mapreduce.Job:  map 86% reduce 0%
19/02/14 10:21:59 INFO mapreduce.Job:  map 90% reduce 0%
19/02/14 10:22:00 INFO mapreduce.Job:  map 92% reduce 0%
19/02/14 10:22:05 INFO mapreduce.Job:  map 97% reduce 0%
19/02/14 10:22:08 INFO mapreduce.Job:  map 98% reduce 0%
19/02/14 10:22:09 INFO mapreduce.Job:  map 100% reduce 0%
19/02/14 10:22:09 INFO mapreduce.Job: Job job_1550131648250_0002 completed successfully
19/02/14 10:22:10 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=598304
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=344
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=170496
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=170496
		Total vcore-milliseconds taken by all map tasks=170496
		Total megabyte-milliseconds taken by all map tasks=174587904
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=344
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1145
		CPU time spent (ms)=122360
		Physical memory (bytes) snapshot=854601728
		Virtual memory (bytes) snapshot=6359822336
		Total committed heap usage (bytes)=948436992
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=10000000000

# terasort
[centos@ip-172-31-34-255 ~]$ sudo -u zdenekapt  hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort   -Ddfs.block.size=32000000 -Dmapred.map.tasks=4 /user/zdenekapt/10-gb-file /user/zdenekapt/10-gb-sorted
19/02/14 10:25:30 INFO terasort.TeraSort: starting
19/02/14 10:25:31 INFO input.FileInputFormat: Total input paths to process : 4
Spent 198ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 202ms
Sampling 10 splits of 316
Making 8 from 100000 sampled records
Computing parititions took 556ms
Spent 760ms computing partitions.
19/02/14 10:25:32 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-34-255.eu-central-1.compute.internal/172.31.34.255:8032
19/02/14 10:25:32 INFO mapreduce.JobSubmitter: number of splits:316
19/02/14 10:25:32 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/02/14 10:25:32 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
19/02/14 10:25:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1550131648250_0003
19/02/14 10:25:33 INFO impl.YarnClientImpl: Submitted application application_1550131648250_0003
19/02/14 10:25:33 INFO mapreduce.Job: The url to track the job: http://ip-172-31-34-255.eu-central-1.compute.internal:8088/proxy/application_1550131648250_0003/
19/02/14 10:25:33 INFO mapreduce.Job: Running job: job_1550131648250_0003
19/02/14 10:25:38 INFO mapreduce.Job: Job job_1550131648250_0003 running in uber mode : false
19/02/14 10:25:38 INFO mapreduce.Job:  map 0% reduce 0%
19/02/14 10:25:46 INFO mapreduce.Job:  map 1% reduce 0%
19/02/14 10:25:48 INFO mapreduce.Job:  map 3% reduce 0%
19/02/14 10:25:49 INFO mapreduce.Job:  map 4% reduce 0%
19/02/14 10:25:54 INFO mapreduce.Job:  map 5% reduce 0%
19/02/14 10:25:57 INFO mapreduce.Job:  map 7% reduce 0%
19/02/14 10:25:58 INFO mapreduce.Job:  map 8% reduce 0%
19/02/14 10:25:59 INFO mapreduce.Job:  map 9% reduce 0%
19/02/14 10:26:05 INFO mapreduce.Job:  map 10% reduce 0%
19/02/14 10:26:06 INFO mapreduce.Job:  map 12% reduce 0%
19/02/14 10:26:08 INFO mapreduce.Job:  map 13% reduce 0%
19/02/14 10:26:11 INFO mapreduce.Job:  map 14% reduce 0%
19/02/14 10:26:15 INFO mapreduce.Job:  map 15% reduce 0%
19/02/14 10:26:16 INFO mapreduce.Job:  map 17% reduce 0%
19/02/14 10:26:21 INFO mapreduce.Job:  map 18% reduce 0%
19/02/14 10:26:24 INFO mapreduce.Job:  map 19% reduce 0%
19/02/14 10:26:25 INFO mapreduce.Job:  map 21% reduce 0%
19/02/14 10:26:26 INFO mapreduce.Job:  map 22% reduce 0%
19/02/14 10:26:32 INFO mapreduce.Job:  map 23% reduce 0%
19/02/14 10:26:34 INFO mapreduce.Job:  map 25% reduce 0%
19/02/14 10:26:35 INFO mapreduce.Job:  map 26% reduce 0%
19/02/14 10:26:38 INFO mapreduce.Job:  map 27% reduce 0%
19/02/14 10:26:42 INFO mapreduce.Job:  map 28% reduce 0%
19/02/14 10:26:43 INFO mapreduce.Job:  map 30% reduce 0%
19/02/14 10:26:45 INFO mapreduce.Job:  map 31% reduce 0%
19/02/14 10:26:50 INFO mapreduce.Job:  map 32% reduce 0%
19/02/14 10:26:51 INFO mapreduce.Job:  map 33% reduce 0%
19/02/14 10:26:52 INFO mapreduce.Job:  map 34% reduce 0%
19/02/14 10:26:55 INFO mapreduce.Job:  map 35% reduce 0%
19/02/14 10:26:58 INFO mapreduce.Job:  map 36% reduce 0%
19/02/14 10:27:00 INFO mapreduce.Job:  map 38% reduce 0%
19/02/14 10:27:01 INFO mapreduce.Job:  map 39% reduce 0%
19/02/14 10:27:05 INFO mapreduce.Job:  map 40% reduce 0%
19/02/14 10:27:09 INFO mapreduce.Job:  map 41% reduce 0%
19/02/14 10:27:10 INFO mapreduce.Job:  map 43% reduce 0%
19/02/14 10:27:12 INFO mapreduce.Job:  map 44% reduce 0%
19/02/14 10:27:18 INFO mapreduce.Job:  map 45% reduce 0%
19/02/14 10:27:19 INFO mapreduce.Job:  map 47% reduce 0%
19/02/14 10:27:20 INFO mapreduce.Job:  map 48% reduce 0%
19/02/14 10:27:26 INFO mapreduce.Job:  map 49% reduce 0%
19/02/14 10:27:28 INFO mapreduce.Job:  map 51% reduce 0%
19/02/14 10:27:29 INFO mapreduce.Job:  map 52% reduce 0%
19/02/14 10:27:34 INFO mapreduce.Job:  map 53% reduce 0%
19/02/14 10:27:37 INFO mapreduce.Job:  map 55% reduce 0%
19/02/14 10:27:38 INFO mapreduce.Job:  map 56% reduce 0%
19/02/14 10:27:41 INFO mapreduce.Job:  map 57% reduce 0%
19/02/14 10:27:46 INFO mapreduce.Job:  map 58% reduce 0%
19/02/14 10:27:47 INFO mapreduce.Job:  map 60% reduce 0%
19/02/14 10:27:48 INFO mapreduce.Job:  map 61% reduce 0%
19/02/14 10:27:54 INFO mapreduce.Job:  map 62% reduce 0%
19/02/14 10:27:55 INFO mapreduce.Job:  map 64% reduce 0%
19/02/14 10:27:56 INFO mapreduce.Job:  map 65% reduce 0%
19/02/14 10:28:01 INFO mapreduce.Job:  map 66% reduce 0%
19/02/14 10:28:02 INFO mapreduce.Job:  map 67% reduce 0%
19/02/14 10:28:04 INFO mapreduce.Job:  map 68% reduce 0%
19/02/14 10:28:05 INFO mapreduce.Job:  map 69% reduce 0%
19/02/14 10:28:08 INFO mapreduce.Job:  map 70% reduce 0%
19/02/14 10:28:10 INFO mapreduce.Job:  map 71% reduce 0%
19/02/14 10:28:13 INFO mapreduce.Job:  map 72% reduce 0%
19/02/14 10:28:14 INFO mapreduce.Job:  map 73% reduce 0%
19/02/14 10:28:16 INFO mapreduce.Job:  map 74% reduce 0%
19/02/14 10:28:18 INFO mapreduce.Job:  map 75% reduce 0%
19/02/14 10:28:22 INFO mapreduce.Job:  map 76% reduce 0%
19/02/14 10:28:23 INFO mapreduce.Job:  map 77% reduce 0%
19/02/14 10:28:24 INFO mapreduce.Job:  map 78% reduce 0%
19/02/14 10:28:27 INFO mapreduce.Job:  map 79% reduce 0%
19/02/14 10:28:30 INFO mapreduce.Job:  map 80% reduce 0%
19/02/14 10:28:31 INFO mapreduce.Job:  map 81% reduce 0%
19/02/14 10:28:32 INFO mapreduce.Job:  map 82% reduce 0%
19/02/14 10:28:35 INFO mapreduce.Job:  map 83% reduce 0%
19/02/14 10:28:38 INFO mapreduce.Job:  map 84% reduce 0%
19/02/14 10:28:42 INFO mapreduce.Job:  map 85% reduce 0%
19/02/14 10:28:47 INFO mapreduce.Job:  map 86% reduce 0%
19/02/14 10:28:48 INFO mapreduce.Job:  map 86% reduce 4%
19/02/14 10:28:49 INFO mapreduce.Job:  map 86% reduce 6%
19/02/14 10:28:50 INFO mapreduce.Job:  map 86% reduce 13%
19/02/14 10:28:51 INFO mapreduce.Job:  map 87% reduce 17%
19/02/14 10:28:53 INFO mapreduce.Job:  map 87% reduce 20%
19/02/14 10:28:55 INFO mapreduce.Job:  map 88% reduce 21%
19/02/14 10:28:56 INFO mapreduce.Job:  map 88% reduce 25%
19/02/14 10:28:57 INFO mapreduce.Job:  map 89% reduce 25%
19/02/14 10:28:59 INFO mapreduce.Job:  map 89% reduce 26%
19/02/14 10:29:01 INFO mapreduce.Job:  map 90% reduce 26%
19/02/14 10:29:03 INFO mapreduce.Job:  map 91% reduce 26%
19/02/14 10:29:08 INFO mapreduce.Job:  map 92% reduce 27%
19/02/14 10:29:11 INFO mapreduce.Job:  map 93% reduce 27%
19/02/14 10:29:14 INFO mapreduce.Job:  map 94% reduce 27%
19/02/14 10:29:17 INFO mapreduce.Job:  map 95% reduce 27%
19/02/14 10:29:20 INFO mapreduce.Job:  map 96% reduce 28%
19/02/14 10:29:24 INFO mapreduce.Job:  map 97% reduce 28%
19/02/14 10:29:27 INFO mapreduce.Job:  map 98% reduce 28%
19/02/14 10:29:30 INFO mapreduce.Job:  map 99% reduce 28%
19/02/14 10:29:31 INFO mapreduce.Job:  map 99% reduce 29%
19/02/14 10:29:33 INFO mapreduce.Job:  map 100% reduce 29%
19/02/14 10:29:36 INFO mapreduce.Job:  map 100% reduce 33%
19/02/14 10:29:37 INFO mapreduce.Job:  map 100% reduce 37%
19/02/14 10:29:38 INFO mapreduce.Job:  map 100% reduce 55%
19/02/14 10:29:41 INFO mapreduce.Job:  map 100% reduce 59%
19/02/14 10:29:43 INFO mapreduce.Job:  map 100% reduce 61%
19/02/14 10:29:44 INFO mapreduce.Job:  map 100% reduce 63%
19/02/14 10:29:45 INFO mapreduce.Job:  map 100% reduce 69%
19/02/14 10:29:46 INFO mapreduce.Job:  map 100% reduce 76%
19/02/14 10:29:47 INFO mapreduce.Job:  map 100% reduce 78%
19/02/14 10:29:49 INFO mapreduce.Job:  map 100% reduce 80%
19/02/14 10:29:50 INFO mapreduce.Job:  map 100% reduce 82%
19/02/14 10:29:51 INFO mapreduce.Job:  map 100% reduce 89%
19/02/14 10:29:52 INFO mapreduce.Job:  map 100% reduce 92%
19/02/14 10:29:53 INFO mapreduce.Job:  map 100% reduce 94%
19/02/14 10:29:54 INFO mapreduce.Job:  map 100% reduce 98%
19/02/14 10:29:58 INFO mapreduce.Job:  map 100% reduce 100%
19/02/14 10:29:59 INFO mapreduce.Job: Job job_1550131648250_0003 completed successfully
19/02/14 10:29:59 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=4445493519
		FILE: Number of bytes written=8837156371
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000051192
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=972
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters
		Launched map tasks=316
		Launched reduce tasks=8
		Data-local map tasks=316
		Total time spent by all maps in occupied slots (ms)=1972815
		Total time spent by all reduces in occupied slots (ms)=573643
		Total time spent by all map tasks (ms)=1972815
		Total time spent by all reduce tasks (ms)=573643
		Total vcore-milliseconds taken by all map tasks=1972815
		Total vcore-milliseconds taken by all reduce tasks=573643
		Total megabyte-milliseconds taken by all map tasks=2020162560
		Total megabyte-milliseconds taken by all reduce tasks=587410432
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4342652990
		Input split bytes=51192
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4342652990
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=200000000
		Shuffled Maps =2528
		Failed Shuffles=0
		Merged Map outputs=2528
		GC time elapsed (ms)=40591
		CPU time spent (ms)=1104910
		Physical memory (bytes) snapshot=167007981568
		Virtual memory (bytes) snapshot=514654871552
		Total committed heap usage (bytes)=187313946624
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=10000000000
	File Output Format Counters
		Bytes Written=10000000000
19/02/14 10:29:59 INFO terasort.TeraSort: done





