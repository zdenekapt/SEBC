# List the cloud provider you are using :
AWS

# List your instances by IP address and DNS name
172-31-47-155 ip-172-31-47-155.eu-central-1.compute.internal ec2-35-156-152-53.eu-central-1.compute.amazonaws.com
172-31-37-70 ip-172-31-37-70.eu-central-1.compute.internal ec2-35-158-118-152.eu-central-1.compute.amazonaws.com
172-31-42-17 ip-172-31-42-17.eu-central-1.compute.internal ec2-18-184-242-255.eu-central-1.compute.amazonaws.com
172-31-33-93 ip-172-31-33-93.eu-central-1.compute.internal ec2-35-158-248-179.eu-central-1.compute.amazonaws.com
172-31-33-116 ip-172-31-33-116.eu-central-1.compute.internal ec2-18-184-213-223.eu-central-1.compute.amazonaws.com

# List the Linux release you are using
CentOS Linux release 7.6.1810 (Core)

# List the file system capacity for the first node
[centos@ip-172-31-47-155 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/nvme0n1p1   30G  1.3G   29G   5% /
devtmpfs        7.6G     0  7.6G   0% /dev
tmpfs           7.6G     0  7.6G   0% /dev/shm
tmpfs           7.6G   17M  7.6G   1% /run
tmpfs           7.6G     0  7.6G   0% /sys/fs/cgroup
tmpfs           1.6G     0  1.6G   0% /run/user/1000

# Yum repositories
[centos@ip-172-31-47-155 ~]$ yum repolist enabled
Failed to set locale, defaulting to C
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: mirror.fra10.de.leaseweb.net
 * extras: mirror.23media.de
 * updates: mirror.fra10.de.leaseweb.net
repo id                                                 repo name                                                 status
base/7/x86_64                                           CentOS-7 - Base                                           10019
extras/7/x86_64                                         CentOS-7 - Extras                                           364
updates/7/x86_64                                        CentOS-7 - Updates                                         1067
repolist: 11450

# /etc/passwd
rocky:x:3800:3800::/home/rocky:/bin/bash
denali:x:3900:3900::/home/denali:/bin/bash

# /etc/group
rocky:x:3800:
denali:x:3900:
alaska:x:3901:denali
colorado:x:3902:rocky

# getent
alaska:x:3901:denali
getent passwd rocky


