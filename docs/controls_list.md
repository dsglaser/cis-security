# CIS Security

## Below are the tags used in the CIS roles on Linux Machines

| RHEL 9 |  RHEL 8 / Fedora 31 / CentOS 8 / Oracle 8 |  RHEL 7 / Centos 7 / Oracle 7  / SLES 15 |  Ubuntu 22.04 | Ubuntu 18.04 / 20.04 | Control Description | Notes |
| ----------------- | -----------------|--------------------- | -----------------|--------------------- | --------------------- | --------------|
|           |  1.1.1.1  |  1.1.1.1  |  1.1.1.1  |  1.1.1.1      |   Remove cramfs |
|           |           |  1.1.1.2  |           |  1.1.1.2      |   Remove freevxfs
|           |           |  1.1.1.3  |           |  1.1.1.3      |   Remove jffs2
|           |           |  1.1.1.4  |           |  1.1.1.4      |   Remove hfs
|           |           |  1.1.1.5  |           |  1.1.1.5      |   Remove hfsplus
|           |  1.1.1.2  |  1.1.1.8  |           |  1.1.1.8      |   Remove vfat
|  1.1.1.1  |  1.1.1.3  |  1.1.1.6  |  1.1.1.2  |  1.1.1.6      |   Remove squashfs
|  1.1.1.2  |  1.1.1.4  |  1.1.1.7  |  1.1.1.3  |  1.1.1.7      |   Remove udf
|   1.1.2   |  1.1.2    |           |  1.1.2    |  1.1.2        |   Ensure tmpfs is configured
|  1.1.2.1  |           |  1.1.2    |  1.1.2.1  |               |   Report if /tmp is not on a separate partition | a) If report comes back saying partitions are not separate, the no\[dev,suid,exec\] checks aren't run b) On a failed control, simply prints a notification to the user |
|  1.1.2.2  |  1.1.3    |  1.1.4    |  1.1.2.2  |  1.1.3        |   Ensure nodev option on /tmp partition
|  1.1.2.3  |  1.1.4    |  1.1.5    |  1.1.2.4  |  1.1.4        |   Ensure nosuid option set on /tmp partition
|  1.1.2.4  |  1.1.5    |  1.1.3    |  1.1.2.3  |  1.1.5        |   Ensure noexec option set on /tmp partition
|   1.1.3   |  1.1.3    |           |  1.1.3    |               |   Configure /var (includes all the /var partition controls)
|  1.1.3.1  |  1.1.3.1  |  1.1.10   |  1.1.3.1  |  1.1.6        |   Report if /var is not on a separate partition
|  1.1.3.2  |  1.1.3.2  |           |  1.1.3.2  |               |   Report if /var is missing nodev option
|  1.1.3.3  |  1.1.3.3  |           |  1.1.3.3  |               |   Report if /var is missing noexec option
|   1.1.4   |   1.1.4   |           |  1.1.4    |               |   Configure /var/tmp
|  1.1.4.1  |  1.1.4.1  |  1.1.11   |  1.1.4.1  |  1.1.7        |   Report if  /var/tmp is not on a separate partition  a) If report comes back saying partitions are not separate, the no\[dev,suid,exec\] checks aren't run b) On a failed control, simply prints a notification to the user |
|  1.1.4.2  |  1.1.4.2  |  1.1.13   |  1.1.4.4  |  1.1.8        |   Ensure nodev option on /var/tmp partition
|  1.1.4.3  |  1.1.4.3  |  1.1.14   |  1.1.4.3  |  1.1.9        |   Ensure nosuid option set on /var/tmp partition
|  1.1.4.4  |  1.1.4.4  |  1.1.12   |  1.1.4.2  |  1.1.10       |   Ensure noexec option set on /var/tmp partition
|   1.1.5   |   1.1.5   |           |  1.1.5    |               |   Configure /var/log
|  1.1.5.1  |  1.1.5.1  |  1.1.15   |  1.1.5.1  |  1.1.11       |   Report if /var/log is not on a separate partition | On a failed control, simply prints a notification to the user |
|  1.1.5.2  |  1.1.5.2  |           |  1.1.5.2  |               |   Ensure nodev option on /var/log partition
|  1.1.5.3  |  1.1.5.3  |           |  1.1.5.4  |               |   Ensure nosuid option set on /var/log partition
|  1.1.5.4  |  1.1.5.4  |           |  1.1.5.3  |               |   Ensure noexec option set on /var/log partition
|   1.1.6   |   1.1.6   |           |  1.1.6    |               |   Configure /var/log/audit
|  1.1.6.1  |  1.1.6.1  |  1.1.16   |  1.1.6.1  |  1.1.12       |   Report if /var/log/audit is not on a separate partition | On a failed control, simply prints a notification to the user |
|  1.1.6.2  |  1.1.6.2  |           |  1.1.6.3  |               |   Ensure nodev option on /var/log/audit partition
|  1.1.6.3  |  1.1.6.3  |           |  1.1.6.4  |               |   Ensure nosuid option set on /var/log/audit partition
|  1.1.6.4  |  1.1.6.4  |           |  1.1.6.2  |               |   Ensure noexec option set on /var/log/audit partition
|   1.1.7   |   1.1.7   |           |  1.1.7    |               |   Configure /home
|  1.1.7.1  |  1.1.7.1  |  1.1.17   |  1.1.7.1  |  1.1.13       |   Report if /home is not on a separate partition | On a failed control, simply prints a notification to the user |
|  1.1.7.2  |  1.1.7.2  |           |  1.1.7.2  |               |   Ensure nodev option on /home partition
|  1.1.7.3  |  1.1.7.3  |           |  1.1.7.3  |               |   Ensure nosuid option set on /home partition
|  1.1.8.2  |  1.1.8.2   |  1.1.8   |  1.1.8.1  |  1.1.15       |   Report if /dev/shm does not have nodev set
|           |            |          |  1.1.8.2  |               |   Report if /dev/shm does not have noexec set
|  1.1.8.2  |  1.1.8.3   |  1.1.9   |  1.1.8.3  |  1.1.16       |   Report if /dev/shm does not have nosuid set
|  1.1.8.4  |  1.1.8.4   |  1.1.20  |           |  1.1.18       |   Ensure nodev option set on removable media | skipped: environment dependent|
|           |  1.1.22   |  1.1.23   |  1.1.9    |  1.1.22       |   Disable automounting
|           |  1.1.23   |  1.1.24   |  1.1.10   |  1.1.23       |   Disable USB storage module
|    1.2.0  |   1.2.0   |           |  1.9.0    |               |  Update System to latest
|           |  1.2.1    |  1.2.2    |  1.2.1    |  1.2.1        |   Ensure system is configured for updates |skipped: environment dependent|
|           |  1.2.2    |  1.2.5    |           |               |   Disable the rhnsd Daemon | RHEL control only |
|  1.2.1  |  1.2.3    |  1.2.1,3  |  1.2.2   |  1.2.2        |   Ensure gpg keys are configured | gpgcheck set to yes. 1.2.2 on SLES 15, but skipped |
|  1.2.2  |  1.2.4    |  1.2.2    |  1.2.2   |  1.2.2        |   Ensure gpgcheck is globally activated. Missing on SLES 15 benchmark
|  1.2.3  |  1.2.5    |  1.2.4    |          |               |   Ensure machine is registerd with Red Hat |skipped: environment dependent|
|  5.3.1  |  5.3.1    |           |  5.3.1   |  1.3.1        |   Ensure sudo is installed
|  5.3.2  |  5.3.2    |           |  5.3.2   |  1.3.2        |   Ensure sudo commands use pty
|  5.3.3  |  5.3.3    |           |  5.3.3   |  1.3.3        |   Ensure sudo log file exists
|  1.3.0  |  1.3.0    |  1.3.0    |  1.3.0   |  1.4.0        |   Install and configure filesystem integrity checking w/AIDE
|  1.3.1  |  1.3.1    |  1.3.1    |  1.3.1   |  1.4.1        |   Ensure aide is installed
|  1.3.2  |  1.3.2    |  1.3.2    |  1.3.2   |  1.4.2        |   Ensure File integrity is regularly checked
|  1.4.1  |  1.4.1    |  1.4.1    |  1.4.1   |  1.5.2        |   Ensure bootloader password is set |skipped: environment dependent|
|  1.4.2  |  1.4.2    |  1.4.2    |  1.4.2   |  1.5.1        |   Set permissions on grub bootloader files
|         |           |  1.4.3    |  1.4.3   |  1.5.3        |   Set single user password | if root password is not set, sets root password before setting up secure single user mode. Uses root_password variable. See [Using vaults with playbooks](https://docs.ansible.com/ansible/latest/user_guide/playbooks_vault.html#playbooks-vault) for information on how to secure it|
|  1.5.1  |  1.5.1    |  1.5.1    |  1.5.4   |  1.6.4        |   Ensure core dumps are restricted
|  1.5.2  |  1.5.2    |           |          |               |   Ensure core dump backtraces are disabled
|         |           |  1.5.2    |          |  1.6.1        |   Ensure XD/NX support is enabled
|  1.5.3  |  1.5.3    |  1.5.3    |  1.5.1   |  1.6.2        |   Ensure address space layout reandomization (ASLR) is enabled
|         |           |  1.5.4    |  1.5.2   |               |   Ensure prelink is not installed
|         |           |           |  1.5.3   |               |   Ensure Apport Error Reporting Service is disabled
|  1.6.0  |  1.6.0    |  1.6.0 \(SLES: skipped\) | | | Configure SELinux | SLES supports SELinux, but does not provide a policy, so enabling it will crash the system, so we are skipping it on SLES)
|  1.6.1.1  |  1.6.1.1  |  1.6.1.1  |           |               |   Ensure SELinux is installed
|  1.6.1.2  |  1.6.1.2  |  1.6.1.2  |           |               |   Ensure SELinux is not disabled in bootloader configuration
|  1.6.1.3  |  1.6.1.3  |  1.6.1.3  |           |               |   Set SELinux policy
|  1.6.1.4  |  1.6.1.4  |  1.6.1.2  |           |               |   Set SELinux to not disabled
|  1.6.1.5  |  1.6.1.5  |  1.6.1.2  |           |               |   Set SELinux state to enforcing
|  1.6.1.6  |  1.6.1.5  |  1.6.1.6  |           |               |   Ensure no unconfined services exist
|  1.6.1.7  |  1.6.1.7  |  1.6.1.7  |           |               |   Remove setroubleshoot
|  1.6.1.8  |  1.6.1.8  |  1.6.1.8  |           |               |   Remove MCS Translation Service
|           |           |           |  1.6.1.0  |  1.7.0        |   Install and Configure AppArmor
|           |           |           |  1.6.1.1  |  1.7.1.1      |   Ensure AppArmor is installed
|           |           |           |  1.6.1.2  |  1.7.1.2      |   Ensure AppArmor is not disabled in bootloader configuration
|           |           |           |  1.6.1.3  |  1.7.1.3      |   Ensure AppArmor profiles are in enforce or complain mode
|           |           |  \(SLES 1.|6.2.2\) | 1.6.1.4 |  1.7.1.4      |   Ensure AppArmor profiles are enforcing | SLES only control in the RHEL 7 file, use 1.6.2.2 for the tag number
|           |           |   \(SLES 1.6.3\)  |         |         |   Ensure SELinux or AppArmor are installed | SLES only control in the RHEL 7 file, use 1.6.3 for the tag number
|  1.7.1  |  1.7.1  |  1.7.1.1  |  1.7.1  |  1.8.1.1  |   Install motd banners
|  1.7.2  |  1.7.2  |  1.7.2    |  1.7.2  |  1.8.1.2  |   Install issue banners
|  1.7.3  |  1.7.3  |  1.7.3    |  1.7.3  |  1.8.1.3  |   Install issue.net banners
|  1.7.4  |  1.7.4  |  1.7.4    |  1.7.4  |  1.8.1.4  |   Ensure permissions on /etc/motd are configured
|  1.7.5  |  1.7.5  |  1.7.5    |  1.7.5  |  1.8.1.5  |   Ensure permissions on /etc/issue are configured
|  1.7.6  |  1.7.6  |  1.7.6    |  1.7.6  |  1.8.1.6  |   Ensure permissions on /etc/issue.net are configured
|  1.8.1  |  1.8.1  |  1.8.1    |  1.8.1  |           |   Ensure GNOME Display Manager is removed
|  1.8.2  |  1.8.2  |  1.8.2    |  1.8.2  |  1.8.2    |   Ensure GDM banner set up
|  1.8.3  |         |  1.8.3    |  1.8.3  |           |   Ensure last logged in user display is disabled
|  1.8.4  |         |           |  1.8.4  |           |   Ensure GDM screen locks when user is idle
|  1.9.0  |  1.9.0  |           |  1.9.0  |  1.9.0    |   Ensure updated system | First control to be run chronologically in order to make sure things are in the same state for the rest of the play
|  1.10.0  |  1.10.0  |           |         |          |   Ensure crypto policy is not legacy | set to what the crypto_policy variable is set to|
|          |  2.1.1   |  2.1.7 \(SL         ES 2.1.11 ||  2.1.1        |   Remove xinetd service
|          |          |  2.1.1    |         |         |   Ensure chagen services are not enabled
|  2.2.1   |  2.2.2   |           |         |         |   Ensure xorg-x11-server-common is not installed
|          |          |  2.1.2    |         |         |   Ensure daytime services are not enabled
|          |          |           |         |  2.1.2  |   Ensure openbsd-inetd is not installed
|          |          |  2.1.3    |         |         |   Ensure discard services are not enabled
|          |          |  2.1.4    |         |         |   Ensure echo services are not enabled
|          |          |  2.1.5    |         |         |   Ensure time services are not enabled
|  2.2.7   |  2.2.9   |  2.1.6    |         |         |   Ensure tftp server is not enabled
|  2.1.1   |  2.1.1   |  2.2.1.1  |  2.1.1  |  2.2.1.1  |   Verify Time synchronization is in use
|          |          |           | 2.1.1.1 |           |   Ensure a single time synchronization daemon is in use
|  2.1.2   |  2.1.2   |  2.2.1.3  |  2.1.2  |  2.2.1.3  |   Configure chrony
|          |          |           | 2.1.2.2 |           |   Ensure chrony is running as user _chrony (configurable via variable)
|          |          |           | 2.1.2.3 |           |   Ensure chrony is enabled and running
|          |          |           |  2.1.3  |  2.2.1.2  |   Configure systemd-timesyncd
|          |          |           | 2.1.3.2 |           |   Ensure systemd_tiemsyncd is enbled and running
|          |          |  2.2.1.2  |         |           |   Configure ntp (skipped on ubuntu as not recommended )
|          |          |  2.2.2    |  2.2.1  |  2.2.2    |   Disable display manager
|  2.2.18  |  2.2.20  |  2.2.21 \(SLES 2.2.18\) |  2.2.16 |  2.2.16  |   Remove rsync
|  2.2.2   |  2.2.3   |  2.2.3    |  2.2.2  |  2.2.3   |   Remove avahi
|  2.2.12  |  2.2.14  |  2.2.14   |  2.2.13 |  2.2.14  |   Remove snmp
|  2.2.11  |  2.2.13  |  2.2.13   |  2.2.12 |  2.2.13  |   Remove Web proxy
|  2.2.10  |  2.2.12  |  2.2.12   |  2.2.11 |  2.2.12  |   Remove Samba server
|  2.2.9   |  2.2.11  |  2.2.11   |  2.2.15 |  2.2.11  |   Remove Mail Relay Server
|  2.2.8   |  2.2.10  |  2.2.10   |  2.2.9  |  2.2.10  |   Remove http Server
|  2.2.6   |  2.2.\[7,8\]  |  2.2.9    | 2.2.8 |  2.2.9    |   Remove FTP Server
|  2.2.5   |  2.2.6   |  2.2.8    |  2.2.7  |  2.2.8    |   Remove DNS server
|  2.2.\[12,16\] |  2.2.18   |  2.2.7    |  2.2.6  |  2.2.7   |   Remove nfs server
|  2.2.16  |  2.2.19  |  2.2.7    |  2.2.6  |  2.2.7   |   Remove rpcbind
|          |  2.2.14  |  2.2.6    |  2.2.5  |  2.2.6   |   Remove LDAP server |skipped in RHEL 8 as it is part of SSSD|
|  2.2.4   |  2.2.5   |  2.2.5    |  2.2.4  |  2.2.5   |   Remove DHCP server
|          |          |  2.2.17   |  2.3.2  |  2.3.2   |   Remove rsh Server/Client
|          |          |  2.2.18   |  2.3.3  |  2.3.3   |   Remove talk
|  2.3.3   |  2.2.9  |  2.2.20 \(SLES 2.2.17\) |  |    |   Remove tftp client
|  2.3.4   |         |            |         |          |  Remove ftp client
|  2.2.3   |  2.2.16 |  2.2.4     |  2.2.3  |  2.2.4   |   Disable cups as we my not be able to uninstall it
|          |  2.2.15 |  2.2.16    | 2.2.14  |  2.2.17  |   Remove NIS Server
|          |  2.2.16 |            |         |          |   Remove telnet-server
|  2.2.15  |  2.2.17 |  2.2.15    | 2.2.15  |  2.2.15  |   Configure mail MTA agent for local-only mode
|          |  2.3.1  |            |  2.3.1  |  2.3.1   |   Remove NIS Client
|  2.3.3   |         |            |         |          |   Remove NFS Client
|  2.3.1   |  2.3.2  |  2.2.19 \(SLES 2.2.8\)  | 2.3.4 | 2.3.4 |   Remove telnet client
|  2.3.2   |  2.3.3  |            |  2.3.5  |  2.3.5    |   Remove openldap-clients
|          |         |            |  3.2.0  |  3.1.0        |   Set host network parameters | host with single interface, or multiple interfaces but not routing between them
|  3.2.1   |  3.1.1  |  3.1.1     |  3.2.2  |  3.1.2        |   Ensure IP forwarding is disabled | included in 3.1.0
|  3.2.2   |  3.1.2  |  3.1.2     |  3.2.1  |  3.1.1        |   Ensure packet redirect sending is disabled | included in 3.1.0
|          |         |            |         |  3.2.0        |   Set host with router network parameters | to be used when using 3.1.0 above as well as hosts with two interfaces configured to perform routing between them
|  3.3.1   |  3.2.1    |  3.2.1   |  3.3.1  |  3.2.1        |   Ensure source routed packets are not accepted | included in 3.2.0
|  3.3.2   |  3.2.2    |  3.2.2,3.3.2 |  3.3.2  | 3.2.2    |   Ensure ICMP redirects are not accepted | included in 3.2.0
|  3.3.3   |  3.2.3    |  3.2.3   |  3.3.3  |  3.2.3        |   Ensure secure ICMP redirects are not accepted | included in 3.2.0
|  3.3.4   |  3.2.4    |  3.2.4   |  3.3.4  |  3.2.4        |   Ensure suspicious packets are logged | included in 3.2.0
|  3.3.5   |  3.2.5    |  3.2.5   |  3.3.5  |  3.2.5        |   Ensure broadcast ICMP requests are ignored | included in 3.2.0
|  3.3.6   |  3.2.6    |  3.2.6   |  3.3.6  |  3.2.6        |   Ensure bogus ICMP responses are ignored | included in 3.2.0
|  3.3.7   |  3.2.7    |  3.2.7   |  3.3.7  |  3.2.7        |   Ensure Reverse Path Filtering is enabled | included in 3.2.0
|  3.3.8   |  3.2.8    |  3.2.8   |  3.3.8  |  3.2.8        |   Ensure TCP SYN Cookies is enabled | included in 3.2.0
|          |           |  3.3.0   |         |               |   IPv6 controls and settings | in RHEL 7 these are in their own area
|  3.3.9   |  3.2.9    |  3.3.1   |  3.3.9  |  3.2.9        |   Ensure IPv6 router advertisements are not accepted
|          |           |  3.3.2   |         |               |   Ensure IPv6 redirects are not accepted | included in 3.2.2 in RHEL8 and Ubuntu |
|          |           |  3.4.1   |         |  3.3.1        |   Install TCPwrappers
|          |           |  3.4.2   |         |  3.3.2        |   Ensure /etc/hosts.allow is configured
|          |           |  3.4.3   |         |  3.3.3        |   Ensure /etc/hosts.deny is configured
|          |           |  3.4.4   |         |  3.3.4        |   Ensure permissions on /etc/hosts.allow
|          |           |  3.4.5   |         |  3.3.5        |   Ensure permissions on /etc/hosts.deny
|  3.1.2   |  3.1.2    |  3.5.2   |  3.4.2  |  3.4.2        |   Ensure SCTP is disabled
|  3.1.3   |  3.1.3    |  3.5.1   |  3.4.1  |  3.4.1        |   Ensure DCCP is disabled
|  3.1.4   |  3.1.4    |  3.5.4   |  3.4.4  |  3.4.4        |   Ensure TIPC is disabled
|          |           |  3.5.3   |  3.4.3  |  3.4.3        |   Ensure RDS is disabled
|  3.4.1.2 |           |  3.6.1   |         |  3.5.1.1      |   Ensure a firewall package is installed (firewalld or iptables)
|          |           |  3.6.2-5 |         |               |   Ensure firewall is configured
|          |           |          |         |               |   firewalld: Ensure firewalld is enabled and running
|          |           |          |         |               |   firewalld: Disable iptables service
|          |           |          |         |               |   firewalld: Disable netfilters service
|          |           |          |         |               |   firewalld: Ensure default zone is set for firewalld
|  3.4.2.1 |           |          |         |               |   firewalld: Set default zone in firewalld
|          |           |          |         |               |   firewalld: Ensure network interfaces are assigned to appropriate zone |skipped: machine dependent|
|  3.4.2   |  3.4.1    |          |         |               |   firewalld: Configure firewalld (block tag)
|          |  3.4.1.1  |          |         |               |   firewalld: Ensure firewalld is installed
|          |  3.4.1.2  |          |         |               |   firewalld: Ensure iptables-services is not installed
|          |  3.4.1.3  |          |         |               |   firewalld: Ensure nftables either not installed or masked with firewalld
|          |  3.4.1.4  |          |         |               |   firewalld: Ensure firewalld is enabled and running
|  3.4.2.1 |  3.4.1.5  |          |         |               |   firewalld: Ensure firewalld default zone is set
|   3.4.2  |   3.4.2   |          |  3.5.2  |               |   nftables: Configure nftables (block tag)
|  3.4.1.1 |  3.4.2.1  |          | 3.5.2.1 |    3.5.3      |   nftables: Ensure nftables is installed
|  3.4.1.2 |           |          |         |               |   nftables: Ensure a single firewall package package is installed
|          |  3.4.2.2  |          |         |               |   nftables: Ensure firewalld is either uninstalled or masked with nftables
|          |  3.4.2.3  |          |         |               |   nftables: Ensure iptables-services not installed with nftables
|          |           |          | 3.5.2.2 |               |   nftables: Ensure ufw is uninstalled with nftables
|          |           |  3.6.1   | 3.5.2.3 |               |   nftables: Ensure iptables are flushed
|  3.4.2.2 |  3.4.2.5  |          | 3.5.2.4 |               |   nftables: Ensure an nftables table is installed
|  3.4.2.3 |           |          | 3.5.2.5 |               |   nftables: Ensure nftables base chains exist
|  3.4.2.4 |           |          | 3.5.2.6 |               |   nftables: Ensure nftables loopback traffic is configured
|          |           |          | 3.5.2.7 |               |   nftables: Ensure establshed connections are configured
|  3.4.1.1 |  3.4.2.10 |          | 3.5.2.9 |               |   nftables: Ensure nftables is started
|          |  3.4.3    |          | 3.5.3.1 |               |   Configure iptables (block tag)
|          |  3.4.3.1.1|          | 3.5.3.2 |               |   Ensure iptables is installed
|          |  3.4.3.1.2|          | 3.5.3.3 |               |   Ensure nftables is not installed with iptables
|          |  3.4.3.1.3|          | 3.5.3.4 |               |   Ensure firewald is not installed with iptables
|          |           |          | 3.5.1.1 |  3.5.2.1      |   Ensure ufw service is enabled
|          |           |          | 3.5.1.2 |               |   Ensure iptables-persistent is not installed with ufw
|          |           |          | 3.5.1.3 |               |   Ensure ufw service is enabled
|          |           |          | 3.5.1.4 |               |   Ensure ufw loopback traffic is configured
|          |           |  3.6.2-5 |         |  3.5.4        |   Configure iptables (skipped: machine dependent)
|          |  3.6.0    |  3.3.3   |         |  3.7          |   Disable IPv6
|    4.1.0  |   4.1.0   |          | 4.1.0   |             |   Configure Auditing (block tag)
|  4.1.1.1  |  4.1.1.1  |          | 4.1.1.1 |  4.1.1.1    |   Install audit package
|  4.1.1.4  |  4.1.1.2  |  4.1.2   | 4.1.1.2 |  4.1.1.2    |   Enable auditd service
|  4.1.1.2  |  4.1.1.3  |  4.1.3   | 4.1.1.3 |  4.1.1.3    |   Ensure auditing for processes that sart prior to auditd
|  4.1.1.3  |  4.1.1.4  |          | 4.1.1.4 |  4.1.1.4    |   Ensure audit_backlog_limit is sufficient
|  4.1.2.1  |  4.1.2.1  |  4.1.1.1 | 4.1.2.1 |  4.1.2.1    |   Configure audit log storage size
|  4.1.2.2  |  4.1.2.2  |  4.1.1.3 | 4.1.2.2 |  4.1.2.2    |   Ensure audit logs are not automatically deleted
|  4.1.2.3  |  4.1.2.3  |  4.1.1.2 | 4.1.2.3 |  4.1.2.3    |   Ensure system is disabled when audit logs are full
|  4.1.3.1  |  4.1.3.1  |  4.1.15  | 4.1.3.1 |  4.1.14     |   Ensure changes to system administration scope \(sudoers\) is collected
|  4.1.3.2  |  4.1.3.2  |          | 4.1.3.2 |             |   Ensure actions on behalf of another user are collected
|  4.1.3.3  |  4.1.3.3  |  4.1.16  | 4.1.3.3 |  4.1.15     |   Ensure sysadmin actions (sudolog) are collected
|  4.1.3.4  |  4.1.3.4  |  4.1.4   | 4.1.3.4 |  4.1.3      |   Ensure to collect events that modify date/time
|  4.1.3.5  |  4.1.3.5  |  4.1.6   | 4.1.3.5 |  4.1.5      |   Ensure modifications to network environment are collected
|  4.1.3.6  |  4.1.3.6  |  4.1.12  | 4.1.3.6 |  4.1.11     |   Ensure use of privileged commands is collected |skipped: machine dependent|
|  4.1.3.7  |  4.1.3.7  |  4.1.11  | 4.1.3.7 |  4.1.10     |   Ensure unsuccessful unauthorized file access attempts are collected
|  4.1.3.8  |  4.1.3.8  |  4.1.5   | 4.1.3.8 |  4.1.4      |   Ensure events that modify user/group information are collected
|  4.1.3.9  |  4.1.3.9  |  4.1.10  | 4.1.3.9 |  4.1.9      |   Ensure modifications to discretionary access controls are collected
|  4.1.3.10 |  4.1.3.10 |  4.1.13  | 4.1.3.10|  4.1.12     |   Ensure successful file system mounts are collected
|  4.1.3.11 |  4.1.3.11 |  4.1.9   | 4.1.3.11|  4.1.8      |   Ensure session initiation information is collected
|  4.1.3.12 |  4.1.3.12 |  4.1.8   | 4.1.3.12|  4.1.7      |   Ensure system logins and logouts are collected
|  4.1.3.13 |  4.1.3.13 |  4.1.14  | 4.1.3.13|  4.1.13     |   Ensure file deletion events by users are collected
|  4.1.3.14 |  4.1.3.14 |  4.1.7   | 4.1.3.14|  4.1.6      |   Ensure modifications to Mandatory Access Controls are collected
|  4.1.3.15 |  4.1.3.15 |          | 4.1.3.15|             |   Ensure all attempts to use the chcon command are collected
|  4.1.3.16 |  4.1.3.16 |          | 4.1.3.16|             |   Ensure all attempts to use the setfacl command are collected
|  4.1.3.17 |  4.1.3.17 |          | 4.1.3.17|             |   Ensure all attempts to use the chacl command are collected
|  4.1.3.18 |  4.1.3.18 |          | 4.1.3.18|             |   Ensure all attempts to use the usermod command are collected
|  4.1.3.19 |  4.1.3.19 |  4.1.17  | 4.1.3.19|  4.1.16     |   Ensure kernel module loading and unloading is collected
|  4.1.3.20 |  4.1.3.20 |  4.1.18  | 4.1.3.20|  4.1.17     |   Ensure audit configuration is immutable
|  4.1.4.1  |           |          | 4.1.4.1 |             |   Ensure audit log files are mode 0640 more more restrictive
|  4.1.4.2  |           |          | 4.1.4.2 |             |   Ensure only authorized users own audit log files
|  4.1.4.3  |           |          | 4.1.4.3 |             |   Ensure only authorized groups own audit log flies
|           |           |          | 4.1.4.4 |             |   Ensure audit log directory is 0750 or more restrictive
|  4.1.4.5  |           |          | 4.1.4.5 |             |   Ensure audit config files are mode 640 or more restrictive
|  4.1.4.6  |           |          | 4.1.4.6 |             |   Ensure audit config files are owned by user root
|           |           |          | 4.1.4.7 |             |   Ensure audit config files are owned by group root
|  4.1.4.7  |           |          | 4.1.4.8 |             |   Ensure audit tools are mode 0755 or more restrictive
|  4.1.4.9  |           |          | 4.1.4.9 |             |   Ensure audit tools are owned by user root
|  4.1.4.10 |           |          | 4.1.4.10|             |   Ensure audit tools belong to group root
|  4.2.1.1  |  4.2.1.1  |  4.2.3   | 4.2.2.1  |  4.2.1.1   |   rsyslog: Ensure rsyslog is installed
|  4.2.1.2  |  4.2.1.2  |          | 4.2.2.2 |  4.2.1.2    |   rsyslog: Enable rsyslog
|  4.2.1.3  |  4.2.1.3  |          | 4.2.2.3 |             |   rsyslog: Ensure journald is configured to send messages to rsyslog
|  4.2.1.4  |  4.2.1.4  |  4.2.1.3 | 4.2.2.4 |  4.2.1.4    |   rsyslog: Ensure rsyslog default file permissions are configured
|  4.2.1.5  |  4.2.1.5  |  4.2.1.2 | 4.2.2.5 |  4.2.1.3    |   rsyslog: Ensure logging is configured |Only runs if the variable rsyslog_file is set, which it is not set by default|
|  4.2.1.6  |  4.2.1.6  |  4.2.1.4 | 4.2.2.6 |  4.2.1.5    |   rsyslog: Ensure logging is configured to send logs to remote host |skipped: environment dependent|
|  4.2.1.7  |  4.2.1.7  |  4.1.2.5 | 4.2.2.7 |  4.2.1.6    |   rsyslog: Ensure remote rsyslog messages are only accepted on designated log hosts
|           |           |  4.2.2.1 |         |             |   Ensure syslog-ng is configured |skipped: not a Red Hat package|
|           |  4.2.2    |          |  4.2.1  |  4.2.2      |   journald: Configure journald
|  4.2.2.1  |  4.2.2.1  |          | 4.2.1.1 |             |   journald: Configure journald to send logs to a remote log host
|  4.2.2.1.1|  4.2.2.1.1|          | 4.2.1.1.1 |           |   journald: Ensure systemd-journal-remote is installed
|  4.2.2.1.2|  4.2.2.1.2|          | 4.2.1.1.2 |           |   journald: Ensure systemd-journal-remote is configured
|  4.2.2.1.3|  4.2.2.1.3|          | 4.2.1.1.3 |           |   journald: Ensure systmd-journal-remote is enabled
|  4.2.2.1.4|  4.2.2.1.4|          | 4.2.1.1.4 |           |   journald: Ensure journald is not configured to recieve logs from a remote client
|  4.2.2.2  |  4.2.2.2  |          | 4.2.1.2 |             |   journald: Ensure journald service is enabled
|  4.2.2.3  |  4.2.2.3  |          | 4.2.1.3 |  4.2.2.2    |   journald: Ensure journald compresses large files
|  4.2.2.4  |  4.2.2.4  |          | 4.2.1.4 |  4.2.2.3    |   journald: Ensure journald writes to peristent disk
|  4.2.2.5  |  4.2.2.5  |          | 4.2.1.5 |  4.2.2.1    |   journald: Forward journald logs to rsyslog IF rsyslog is sending logs to a log host
|  4.2.3    |  4.2.3    |          |  4.2.3  |             |   Ensure all log files have appropriate permissions and ownership
|  4.3.0    |  4.3.0    |  4.3.0   ||  4.3        |   Ensure logrotate is installed and configured
|  5.1.0    |  5.1.0    |          |  5.1.0  |             |   Configure Cron/At
|  5.1.1    |  5.1.1    |  5.1.1   |  5.1.1  |  5.1.1      |   Ensure cron is enabled
|  5.1.2    |  5.1.2    |  5.1.2   |  5.1.2  |  5.1.2      |   Ensure permissions on /etc/crontab
|  5.1.3    |  5.1.3    |  5.1.3   |  5.1.3  |  5.1.3      |   Ensure permissions on /etc/cron.hourly
|  5.1.4    |  5.1.4    |  5.1.4   |  5.1.4  |  5.1.4      |   Ensure permissions on /etc/cron.daily
|  5.1.5    |  5.1.5    |  5.1.5   |  5.1.5  |  5.1.5      |   Ensure permissions on /etc/cron.weekly
|  5.1.6    |  5.1.6    |  5.1.6   |  5.1.6  |  5.1.6      |   Ensure permissions on /etc/cron.monthly
|  5.1.7    |  5.1.7    |  5.1.7   |  5.1.7  |  5.1.7      |   Ensure permissions on /etc/cron.d
|  5.1.8    |  5.1.8    |          |  5.1.8  |             |   Ensure cron restricted to authorized users
|  5.1.9    |  5.1.9    |          |  5.1.9  |             |   Ensure at restricted to authorized users
|  5.2.1.0  |  5.2.0    |  5.2.0   | 5.2.0   |  5.2.0      |   SSH File configurations
|  5.2.1.1  |  5.2.1    |  5.2.1   | 5.2.1   |  5.2.1      |   Set permissions on SSH file
|  5.2.1.2  |  5.2.2    |          | 5.2.2   |  5.2.2      |   Set Permissions on ssh private host keys
|  5.2.1.3  |  5.2.3    |          | 5.2.3   |  5.2.3      |   Set Permissions on ssh public host keys
|  5.2.1.4  |  5.2.4    |  5.2.14  | 5.2.4   |  5.2.18     |   Ensure SSH access is limited |skipped: environment dependent|
|           |           |  5.2.2   |         |  5.2.4      |   Ensure SSH Protocol is set to 2
|  5.2.1.5  |  5.2.5    |  5.2.3   | 5.2.5   |  5.2.5      |   Set LogLevel to INFO
|  5.2.1.6  |  5.2.6    |  5.2.6   | 5.2.6   |  5.2.20     |   Ensure SSH PAM is enabled
|  5.2.1.7  |  5.2.7    |  5.2.8   | 5.2.7   |  5.2.10     |   Ensure PermitRootLogin is disbled
|  5.2.1.8  |  5.2.8    |  5.2.7   | 5.2.8   |  5.2.9      |   Ensure HostbasedAuthentication is disabled
|  5.2.1.9  |  5.2.9    |  5.2.9   | 5.2.9   |  5.2.11     |   Ensure SSH PermitEmptyPasswords is disabled
|  5.2.1.10 |  5.2.10   |  5.2.10  | 5.2.10  |  5.2.12     |   Ensure PermitUserEnvironment is disabled
|  5.2.1.11 |  5.2.11   |          | 5.2.11  |             |   Ensure IgnoreRhosts is enabled
|  5.2.1.12 |  5.2.12   |  5.2.4   | 5.2.12  |  5.2.6      |   Disable X11 forwarding
|  5.2.1.13 |  5.2.13   |          | 5.2.16  |  5.2.21     |   Disable SSH Forwarding
|  5.2.1.14 |  5.2.14   |          |         |             |   Ensure system crypto policy isn't overriden in SSH
|  5.2.1.15 |  5.2.15   |  5.2.15  | 5.2.17  |  5.2.19     |   Ensure SSH Banner is configured
|  5.2.1.16 |  5.2.16   |  5.2.5   | 5.2.18  |  5.2.7      |   Ensure SSH MaxAuthTires is set
|  5.2.1.17 |  5.2.17   |          | 5.2.19  |  5.2.22     |   Ensure MaxStartups is configured
|  5.2.1.18 |  5.2.18   |          | 5.2.20  |  5.2.23     |   Ensure MaxSessions is set to 10 or less
|  5.2.1.19 |  5.2.19   |  5.2.13  | 5.2.21  |  5.2.17     |   Ensure SSH LoginGraceTime is set
|  5.2.1.20 |  5.2.20   |  5.2.12  | 5.2.22  |  5.2.16     |   Ensure SSH Idle Timeout is configured
|           |           |          | 5.2.13  |  5.2.13     |   Ensure only strong Ciphers are used
|           |           |  5.2.11  | 5.2.14  |  5.2.14     |   Ensure only approved MAC alogrithms are used
|   5.3.0   |  5.3.0    |          | 5.3.0   |             |   Configure privilege escalation
|   5.3.1   |  5.3.1    |          | 5.3.1   |             |   Ensure sudo is installed
|   5.3.2   |  5.3.2    |          | 5.3.2   |             |   Ensure sudo commands use pty
|   5.3.3   |  5.3.3    |          | 5.3.3   |             |   Ensure sudo log file exists
|   5.3.4   |  5.3.4    |          | 5.3.4   |             |   Ensure users must provide password for escalation
|   5.3.5   |  5.3.5    |          | 5.3.5   |             |   Ensure re-authentication for privlege ecalation is not disabled globally
|           |           |          | 5.3.6   |             |   Ensure audo authentication timeout is configured correctly
|   5.3.7   |  5.3.7    |  5.6.0   | 5.3.7   |  5.6        |   Restrict su to wheel group | on Ubuntu control says to any one group, but for simplicity we are using wheel |
|   5.5.1   |  5.5.1    |  5.3.1   | 5.4.1   |  5.3.1      |   Configure PAM files and password requirements
|   5.5.2   |  5.5.2    |          | 5.4.2   |             |   Ensure lockout for failed password attempts
|   5.5.4   |  5.5.4    |          | 5.4.4   |             |   Configure password hashing algorithm is SHA-512 or YESCRIPT
|   5.6.1.1 |  5.6.1.1  |  5.4.1.1 | 5.5.1.1 |  5.4.1.1    |   Ensure password expiration is 365 days or less
|   5.6.1.2 |  5.6.1.2  |  5.4.1.3 | 5.5.1.3 |  5.4.1.3    |   Ensure password warning days is set to 7
|   5.6.1.3 |  5.6.1.3  |  5.4.1.2 | 5.5.1.2 |  5.4.1.2    |   Ensure password change days is set to 7
|   5.6.1.4 |  5.6.1.4  |  5.4.1.4 | 5.5.1.5 |  5.4.1.4    |   Disable accounts that are inactive for 30 days after password expiration
|   5.6.3   |  5.6.3    |  5.4.5   | 5.5.5   |  5.4.5      |   Ensure default shell timeout is 900 seconds or less
|   5.6.4   |  5.6.4    |  5.4.3   | 5.5.3   |  5.4.3      |   Ensure default group for root is GID 0
|   5.6.5   |  5.6.5    |  5.4.4   | 5.5.4   |  5.4.4      |   Ensure default umask is set
|   6.1.1   |  6.1.3    |  6.1.2   |  6.1.1  |   6.1.2     |   Ensure permissions on /etc/passwd
|   6.1.2   |  6.1.7    |  6.1.6   |  6.1.2  |   6.1.6     |   Ensure permissions on /etc/passwd-
|   6.1.3   |  6.1.5    |  6.1.4   |  6.1.3  |   6.1.4     |   Ensure permissions on /etc/group
|   6.1.4   |  6.1.9    |  6.1.8   |  6.1.4  |   6.1.8     |   Ensure permissions on /etc/group-
|   6.1.5   |  6.1.4    |  6.1.3   |  6.1.5  |   6.1.3     |   Ensure permissions on /etc/shadow
|   6.1.6   |  6.1.8    |  6.1.7   |  6.1.6  |   6.1.7     |   Ensure permissions on /etc/shadow-
|   6.1.7   |  6.1.6    |  6.1.5   |  6.1.7  |   6.1.5     |   Ensure permissions on /etc/gshadow
|   6.1.8   |  6.1.10   |  6.1.9   |  6.1.8  |   6.1.9     |   Ensure permissions on /etc/gshadow-
|   6.1.9   |  6.1.11   |  6.1.10  |  6.1.9  |  6.1.10     |   Report if any world writable files exist
|   6.1.10  |  6.1.12   |  6.1.11  |  6.1.10 |  6.1.11     |   Report if any unowned files or directories exist
|   6.1.11  |  6.1.13   |  6.1.12  |  6.1.11 |  6.1.12     |   Report if any ungrouped files or directories exist
|   6.1.12  |  6.1.2    |  1.1.22  |         |  1.1.21     |   Ensure sticky bit on world writable directories
|   6.2.1   |  6.2.2    |          |  6.2.1  |             |   Ensure accounts in /etc/passwd use shadowed passwords
|   6.2.2   |  6.2.1    |  6.2.1   |  6.2.2  |  6.2.1      |   Report on password fields that are empty
|   6.2.3   |           |  6.2.15  |  6.2.3  |  6.2.15     |   Ensure al groups in /etc/passwd exist in /etc/group
|           |           |          |  6.2.4  |             |   Ensure shadow group is empty
|   6.2.4   |  6.2.3    |  6.2.16  |  6.2.5  |  6.2.16     |   Report on duplicate UIDs in /etc/passwd
|   6.2.5   |  6.2.4    |  6.2.17  |  6.2.6  |  6.2.17     |   Report on duplicate GIDs in /etc/group
|   6.2.6   |  6.2.5    |  6.2.18  |  6.2.7  |  6.2.18     |   Report on duplicate users in /etc/passwd
|   6.2.7   |  6.2.6    |  6.2.19  |  6.2.8  |  6.2.19     |   Report on duplicate groups in /etc/group
|   6.2.8   |  6.2.7    |  6.2.6   |  6.2.9  |  6.2.7      |   Ensure root PATH integrity
|   6.2.9   |  6.2.8    |  6.2.5   |  6.2.10 |  6.2.6      |   Report on multiple accounts with UID of 0
|   6.2.10  |  6.2.10   |  6.2.9   |  6.2.11 |  6.2.9      |   Ensure home directories exist |skipped: environment dependent|
|   6.2.11  |  6.2.11   |  6.2.10  |         |  6.2.8      |   Ensure home directory permissions are 750 or more restrictive (skipped: environment dependent|
|           |           |  6.2.2   |         |  6.2.2      |   Ensure no legacy "+" entries exist in /etc/passwd
|           |           |  6.2.3   |         |  6.2.4      |   Ensure no legacy "+" entries exist in /etc/shadow
|           |           |  6.2.4   |         |  6.2.5      |   Ensure no legacy "+" entries exist in /etc/group
|           |           | 6.2.10-14|         |  6.2.10-14  |   Various controls recommended to be run by monitoring software
|           |           |          |         |  6.2.20     |   Report if shadow group exists in /etc/group
