[centos@ip-172-31-37-70 ~]$ sudo -u rocky time  hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Ddfs.block.size=32000000 -Dmapred.map.tasks=8 123450000 /user/rocky/files
19/02/15 10:47:43 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-37-70.eu-central-1.compute.internal/172.31.37.70:8032
19/02/15 10:47:44 INFO terasort.TeraGen: Generating 123450000 using 8
19/02/15 10:47:44 INFO mapreduce.JobSubmitter: number of splits:8
19/02/15 10:47:44 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/02/15 10:47:44 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
19/02/15 10:47:44 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1550225759749_0001
19/02/15 10:47:44 INFO impl.YarnClientImpl: Submitted application application_1550225759749_0001
19/02/15 10:47:44 INFO mapreduce.Job: The url to track the job: http://ip-172-31-37-70.eu-central-1.compute.internal:8088/proxy/application_1550225759749_0001/
19/02/15 10:47:44 INFO mapreduce.Job: Running job: job_1550225759749_0001
19/02/15 10:47:50 INFO mapreduce.Job: Job job_1550225759749_0001 running in uber mode : false
19/02/15 10:47:50 INFO mapreduce.Job:  map 0% reduce 0%
19/02/15 10:48:08 INFO mapreduce.Job:  map 13% reduce 0%
19/02/15 10:48:09 INFO mapreduce.Job:  map 45% reduce 0%
19/02/15 10:48:14 INFO mapreduce.Job:  map 50% reduce 0%
19/02/15 10:48:15 INFO mapreduce.Job:  map 60% reduce 0%
19/02/15 10:48:20 INFO mapreduce.Job:  map 62% reduce 0%
19/02/15 10:48:21 INFO mapreduce.Job:  map 65% reduce 0%
19/02/15 10:48:26 INFO mapreduce.Job:  map 67% reduce 0%
19/02/15 10:48:27 INFO mapreduce.Job:  map 73% reduce 0%
19/02/15 10:48:32 INFO mapreduce.Job:  map 75% reduce 0%
19/02/15 10:48:33 INFO mapreduce.Job:  map 80% reduce 0%
19/02/15 10:48:36 INFO mapreduce.Job:  map 81% reduce 0%
19/02/15 10:48:38 INFO mapreduce.Job:  map 82% reduce 0%
19/02/15 10:48:39 INFO mapreduce.Job:  map 83% reduce 0%
19/02/15 10:48:40 INFO mapreduce.Job:  map 88% reduce 0%
19/02/15 10:48:44 INFO mapreduce.Job:  map 89% reduce 0%
19/02/15 10:48:46 INFO mapreduce.Job:  map 94% reduce 0%
19/02/15 10:48:50 INFO mapreduce.Job:  map 95% reduce 0%
19/02/15 10:48:52 INFO mapreduce.Job:  map 99% reduce 0%
19/02/15 10:48:53 INFO mapreduce.Job:  map 100% reduce 0%
19/02/15 10:48:54 INFO mapreduce.Job: Job job_1550225759749_0001 completed successfully
19/02/15 10:48:54 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=1196232
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=683
		HDFS: Number of bytes written=12345000000
		HDFS: Number of read operations=32
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters
		Launched map tasks=8
		Other local map tasks=8
		Total time spent by all maps in occupied slots (ms)=434429
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=434429
		Total vcore-milliseconds taken by all map tasks=434429
		Total megabyte-milliseconds taken by all map tasks=444855296
	Map-Reduce Framework
		Map input records=123450000
		Map output records=123450000
		Input split bytes=683
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2241
		CPU time spent (ms)=163150
		Physical memory (bytes) snapshot=2439942144
		Virtual memory (bytes) snapshot=12657446912
		Total committed heap usage (bytes)=2477785088
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=265113961663139567
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=12345000000
4.38user 0.21system 1:13.23elapsed 6%CPU (0avgtext+0avgdata 243452maxresident)k
0inputs+1048outputs (0major+76568minor)pagefaults 0swaps



[centos@ip-172-31-37-70 ~]$ hdfs dfs -ls /user/rocky/files
Found 9 items
-rw-r--r--   3 rocky supergroup          0 2019-02-15 10:48 /user/rocky/files/_SUCCESS
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00000
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00001
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00002
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00003
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00004
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00005
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00006
-rw-r--r--   3 rocky supergroup 1543125000 2019-02-15 10:48 /user/rocky/files/part-m-00007


[centos@ip-172-31-37-70 ~]$ hdfs fsck -blocks /user/rocky
Connecting to namenode via http://ip-172-31-37-70.eu-central-1.compute.internal:50070/fsck?ugi=hdfs&blocks=1&path=%2Fuser%2Frocky
FSCK started by hdfs (auth:SIMPLE) from /172.31.37.70 for path /user/rocky at Fri Feb 15 11:05:29 UTC 2019
.........Status: HEALTHY
 Total size:	12345000000 B
 Total dirs:	3
 Total files:	9
 Total symlinks:		0
 Total blocks (validated):	392 (avg. block size 31492346 B)
 Minimally replicated blocks:	392 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		4
 Number of racks:		1
FSCK ended at Fri Feb 15 11:05:29 UTC 2019 in 8 milliseconds