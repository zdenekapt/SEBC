# Swappiness
[centos@ip-172-31-34-255 ~]$ cat /proc/sys/vm/swappiness
1

# Mount attributes
Filesystem      Size  Used Avail Use% Mounted on
/dev/nvme0n1p1   30G   12G   19G  40% /
devtmpfs        7.6G     0  7.6G   0% /dev
tmpfs           7.6G     0  7.6G   0% /dev/shm
tmpfs           7.6G   17M  7.6G   1% /run
tmpfs           7.6G     0  7.6G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/0
tmpfs           1.6G     0  1.6G   0% /run/user/1000
cm_processes    7.6G   13M  7.6G   1% /run/cloudera-scm-agent/process
tmpfs           1.6G     0  1.6G   0% /run/user/997

#hugepage support
[root@ip-172-31-34-255 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]

# Network configuration
[centos@ip-172-31-34-255 ~]$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: ens5: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP group default qlen 1000
    link/ether 06:9b:ae:a7:0e:5a brd ff:ff:ff:ff:ff:ff
    inet 172.31.34.255/20 brd 172.31.47.255 scope global dynamic ens5
       valid_lft 3092sec preferred_lft 3092sec
    inet6 fe80::49b:aeff:fea7:e5a/64 scope link
       valid_lft forever preferred_lft forever

# getent
[centos@ip-172-31-34-255 ~]$ getent hosts ip-172-31-34-255.eu-central-1.compute.internal
fe80::49b:aeff:fea7:e5a ip-172-31-34-255.eu-central-1.compute.internal

#nslookup
[centos@ip-172-31-34-255 ~]$ nslookup ip-172-31-34-255.eu-central-1.compute.internal
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
Name:	ip-172-31-34-255.eu-central-1.compute.internal
Address: 172.31.34.255

#nscd
[centos@ip-172-31-34-255 ~]$ sudo systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2019-02-14 00:34:14 UTC; 7s ago
  Process: 8274 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 8275 (nscd)
   CGroup: /system.slice/nscd.service
           └─8275 /usr/sbin/nscd

Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring directory `/etc` (2)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring file `/etc/hosts` (4)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring directory `/etc` (2)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring file `/etc/resolv.conf` (5)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring directory `/etc` (2)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring file `/etc/services` (6)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 monitoring directory `/etc` (2)
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 disabled inotify-based monitoring f...ry
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal nscd[8275]: 8275 stat failed for file `/etc/netgroup...ry
Feb 14 00:34:14 ip-172-31-34-255.eu-central-1.compute.internal systemd[1]: Started Name Service Cache Daemon.
Hint: Some lines were ellipsized, use -l to show in full.

#ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2019-02-14 00:42:33 UTC; 6s ago
  Process: 9385 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9386 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─9386 /usr/sbin/ntpd -u ntp:ntp -g

Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen and drop on 0 v4wildcard 0.0.0.0 ...23
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen and drop on 1 v6wildcard :: UDP 123
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen normally on 2 lo 127.0.0.1 UDP 123
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen normally on 3 ens5 172.31.34.255 ...23
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen normally on 4 lo ::1 UDP 123
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listen normally on 5 ens5 fe80::49b:aeff...23
Feb 14 00:42:33 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: Listening on routing socket on fd #22 fo...es
Feb 14 00:42:34 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: 0.0.0.0 c016 06 restart
Feb 14 00:42:34 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Feb 14 00:42:34 ip-172-31-34-255.eu-central-1.compute.internal ntpd[9386]: 0.0.0.0 c011 01 freq_not_set
Hint: Some lines were ellipsized, use -l to show in full.





