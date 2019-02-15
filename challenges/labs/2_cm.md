[centos@ip-172-31-37-70 ~]$ ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Sources.repo  CentOS-fasttrack.repo  mariadb.repo
CentOS-CR.repo    CentOS-Media.repo      CentOS-Vault.repo    cloudera-manager.repo


[centos@ip-172-31-37-70 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm cloudera
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/java/postgresql-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!




