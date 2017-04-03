[root@ip-10-79-133-7 ~]# cat /proc/sys/vm/swappiness
1
[root@ip-10-79-133-7 ~]# cat /etc/sysctl.conf
# System default settings live in /usr/lib/sysctl.d/00-system.conf.
# To override those settings, enter new settings here, or in an /etc/sysctl.d/<name>.conf file
#
# For more information, see sysctl.conf(5) and sysctl.d(5).
vm.swappiness = 1

[root@ip-10-79-133-7 ~]# mount -v
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=7599028k,nr_inodes=1899757,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/net_cls type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/xvda1 on / type xfs (rw,relatime,attr2,inode64,noquota)
rpc_pipefs on /var/lib/nfs/rpc_pipefs type rpc_pipefs (rw,relatime)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=31,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime)
nfsd on /proc/fs/nfsd type nfsd (rw,relatime)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,size=1497312k,mode=700,uid=1000,gid=1000)
/dev/xvdb1 on /data type ext4 (rw,relatime,data=ordered)

[root@ip-10-79-133-7 ~]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]

[root@ip-10-79-133-7 ~]# ifconfig 
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.79.133.7  netmask 255.255.255.192  broadcast 10.79.133.63
        inet6 fe80::2000:aff:fe4f:8507  prefixlen 64  scopeid 0x20<link>
        ether 22:00:0a:4f:85:07  txqueuelen 1000  (Ethernet)
        RX packets 603800  bytes 846611288 (807.3 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 245779  bytes 17809463 (16.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@ip-10-79-133-7 ~]# getent hosts
127.0.0.1       localhost.localdomain localhost
127.0.0.1       localhost6.localdomain6 localhost6
10.79.133.7     srvsebclnx01.hadoop.local srvsebclnx01
10.179.235.113  srvsebclnx02.hadoop.local srvsebclnx02
10.180.35.164   srvsebclnx03.hadoop.local srvsebclnx03
10.71.191.242   srvsebclnx04.hadoop.local srvsebclnx04
10.79.131.18    srvsebclnx05.hadoop.local srvsebclnx05

[root@ip-10-79-133-7 ~]# nslookup
> ip-10-79-131-18.ec2.internal
Server:		172.16.0.23
Address:	172.16.0.23#53

Non-authoritative answer:
Name:	ip-10-79-131-18.ec2.internal
Address: 10.79.131.18
> ip-10-71-191-242.ec2.internal
Server:		172.16.0.23
Address:	172.16.0.23#53

Non-authoritative answer:
Name:	ip-10-71-191-242.ec2.internal
Address: 10.71.191.242
> ip-10-180-35-164.ec2.internal
Server:		172.16.0.23
Address:	172.16.0.23#53

Non-authoritative answer:
Name:	ip-10-180-35-164.ec2.internal
Address: 10.180.35.164
> ip-10-179-235-113.ec2.internal
Server:		172.16.0.23
Address:	172.16.0.23#53

Non-authoritative answer:
Name:	ip-10-179-235-113.ec2.internal
Address: 10.179.235.113
> ip-10-79-133-7.ec2.internal
Server:		172.16.0.23
Address:	172.16.0.23#53

Non-authoritative answer:
Name:	ip-10-79-133-7.ec2.internal
Address: 10.79.133.7

[root@ip-10-79-133-7 ~]# systemctl status  nscd.service 
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-04-03 16:40:04 UTC; 11s ago
 Main PID: 22411 (nscd)
   CGroup: /system.slice/nscd.service
           +-22411 /usr/sbin/nscd

Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring directory `/etc` (2)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring file `/etc/hosts` (4)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring directory `/etc` (2)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring file `/etc/resolv.conf` (5)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring directory `/etc` (2)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring file `/etc/services` (6)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 monitoring directory `/etc` (2)
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal nscd[22411]: 22411 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Apr 03 16:40:04 ip-10-79-133-7.ec2.internal systemd[1]: Started Name Service Cache Daemon.

[root@ip-10-79-133-7 ~]# systemctl status ntpd.service
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-04-03 16:43:10 UTC; 11s ago
  Process: 22585 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 22586 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-22586 /usr/sbin/ntpd -u ntp:ntp -g

Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: Listen normally on 2 lo 127.0.0.1 UDP 123
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: Listen normally on 3 eth0 10.79.133.7 UDP 123
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: Listen normally on 4 lo ::1 UDP 123
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: Listen normally on 5 eth0 fe80::2000:aff:fe4f:8507 UDP 123
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: Listening on routing socket on fd #22 for interface updates
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal systemd[1]: Started Network Time Service.
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: 0.0.0.0 c016 06 restart
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Apr 03 16:43:10 ip-10-79-133-7.ec2.internal ntpd[22586]: 0.0.0.0 c011 01 freq_not_set
Apr 03 16:43:17 ip-10-79-133-7.ec2.internal ntpd[22586]: 0.0.0.0 c614 04 freq_mode

