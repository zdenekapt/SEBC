What is ubertask optimization? 
"Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

Where in CM is the Kerberos Security Realm value displayed? 
Administration => Settings => Kerberos

Which CDH service(s) host a property for enabling Kerberos authentication? 
Zookeepere, HDFS, YARN

How do you upgrade the CM agents? 
You can do it through wizard in Cloudera Manager Server https://www.cloudera.com/documentation/enterprise/latest/topics/cm_ag_ug_cm5.html#concept_gs4_bsg_xw

Give the tsquery statement used to chart Hue's CPU utilization? 

Name all the roles that make up the Hive service Gateway? 
Hive Metastore, HiveServer2

What steps must be completed before integrating Cloudera Manager with Kerberos? 
Java Cryptografic Extension installed.
The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. 
CDH will not work properly if tickets are not renewable.
Kerberos client libraries should be installed on ALL hosts.