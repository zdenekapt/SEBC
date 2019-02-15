# Create directory precious, copy file ...
[centos@ip-172-31-34-255 ~]$ sudo -u hdfs hdfs dfs -mkdir /precious
[centos@ip-172-31-34-255 ~]$ sudo -u hdfs hdfs dfs -put /tmp/master.zip /precious

[centos@ip-172-31-34-255 ~]$ hdfs dfs -ls /precious
Found 1 items
-rw-r--r--   3 hdfs supergroup    1155508 2019-02-14 11:56 /precious/master.zip


