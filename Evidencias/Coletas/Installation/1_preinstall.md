[root@ip-172-31-24-87 ~]# hostname && echo && cat /proc/sys/vm/swappiness && echo && cat /etc/sysctl.conf && echo && mount -v && echo && ifconfig && echo && getent hosts && echo && systemctl status nscd.service && echo && systemctl status ntpd.service && echo && ls -lahtr /usr/share/java/mysql-connector-java.jar
ip-172-31-24-87.us-east-2.compute.internal

1

# sysctl settings are defined through files in
# /usr/lib/sysctl.d/, /run/sysctl.d/, and /etc/sysctl.d/.
#
# Vendors settings live in /usr/lib/sysctl.d/.
# To override a whole file, create a new file with the same in
# /etc/sysctl.d/ and put new settings there. To override
# only specific settings, add a file with a lexically later
# name in /etc/sysctl.d/ and put new settings there.
#
# For more information, see sysctl.conf(5) and sysctl.d(5).
vm.swappiness = 1

sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime,seclabel)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,seclabel,size=8112696k,nr_inodes=2028174,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev,seclabel)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,seclabel,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,seclabel,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,seclabel,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/pids type cgroup (rw,nosuid,nodev,noexec,relatime,pids)
cgroup on /sys/fs/cgroup/net_cls,net_prio type cgroup (rw,nosuid,nodev,noexec,relatime,net_prio,net_cls)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/xvda1 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
rpc_pipefs on /var/lib/nfs/rpc_pipefs type rpc_pipefs (rw,relatime)
selinuxfs on /sys/fs/selinux type selinuxfs (rw,relatime)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=23,pgrp=1,timeout=0,minproto=5,maxproto=5,direct,pipe_ino=11128)
mqueue on /dev/mqueue type mqueue (rw,relatime,seclabel)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,seclabel)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
nfsd on /proc/fs/nfsd type nfsd (rw,relatime)
binfmt_misc on /proc/sys/fs/binfmt_misc type binfmt_misc (rw,relatime)
tmpfs on /run/user/0 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1626672k,mode=700)
cm_processes on /run/cloudera-scm-agent/process type tmpfs (rw,relatime,seclabel,mode=751)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,seclabel,size=1626672k,mode=700,uid=1000,gid=1000)

eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.24.87  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::44a:46ff:fea2:44be  prefixlen 64  scopeid 0x20<link>
        ether 06:4a:46:a2:44:be  txqueuelen 1000  (Ethernet)
        RX packets 336195  bytes 78942200 (75.2 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 248217  bytes 51827078 (49.4 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 194005  bytes 122644296 (116.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 194005  bytes 122644296 (116.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


127.0.0.1       localhost localhost.localdomain localhost4 localhost4.localdomain4
127.0.0.1       localhost localhost.localdomain localhost6 localhost6.localdomain6
172.31.30.147   ip-172-31-30-147.us-east-2.compute.internal
172.31.24.87    ip-172-31-24-87.us-east-2.compute.internal
172.31.31.242   ip-172-31-31-242.us-east-2.compute.internal
172.31.19.76    ip-172-31-19-76.us-east-2.compute.internal
172.31.18.153   ip-172-31-18-153.us-east-2.compute.internal

● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2017-12-07 11:07:05 UTC; 6h ago
  Process: 579 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 591 (nscd)
   CGroup: /system.slice/nscd.service
           └─591 /usr/sbin/nscd

Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 monitoring file `/etc/services` (6)
Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 monitoring directory `/etc` (2)
Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 Access Vector Cache (AVC) started
Dec 07 11:07:05 ip-172-31-24-87.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Dec 07 11:07:08 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 monitored file `/etc/resolv.conf` was written to
Dec 07 11:07:08 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 monitoring file `/etc/resolv.conf` (5)
Dec 07 11:07:08 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 monitoring directory `/etc` (2)
Dec 07 11:07:24 ip-172-31-24-87.us-east-2.compute.internal nscd[591]: 591 checking for monitored file `/etc/netgroup': No such file or directory

● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Thu 2017-12-07 17:07:14 UTC; 19s ago
  Process: 9195 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9196 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─9196 /usr/sbin/ntpd -u ntp:ntp -g

Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen and drop on 0 v4wildcard 0.0.0.0 UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen and drop on 1 v6wildcard :: UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen normally on 3 eth0 172.31.24.87 UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen normally on 4 lo ::1 UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listen normally on 5 eth0 fe80::44a:46ff:fea2:44be UDP 123
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: Listening on routing socket on fd #22 for interface updates
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: 0.0.0.0 c016 06 restart
Dec 07 17:07:14 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: 0.0.0.0 c012 02 freq_set kernel 100.822 PPM
Dec 07 17:07:21 ip-172-31-24-87.us-east-2.compute.internal ntpd[9196]: 0.0.0.0 c615 05 clock_sync

-rw-r--r--. 1 root root 864K Jun 10  2014 /usr/share/java/mysql-connector-java.jar




