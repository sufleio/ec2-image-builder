# CIS Benchmarks
This build script is configuring hardening based on CIS Amazon Linux 2 Benchmark version 1.0.0.

https://www.cisecurity.org/benchmark/amazon_linux/

## Benchmark Coverage List
| Benchmark Item                                                                                   | Coverage Status                                    |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------|
| 1 Initial Setup                                                                                  |                                                    |
| 1.1 Filesystem Configuration                                                                     |                                                    |
| 1.1.1 Disable unused filesystems                                                                 |                                                    |
| 1.1.1.1 Ensure mounting of cramfs filesystems is disabled (Scored)                               | implemented                                        |
| 1.1.1.2 Ensure mounting of hfs filesystems is disabled (Scored)                                  | implemented                                        |
| 1.1.1.3 Ensure mounting of hfsplus filesystems is disabled (Scored)                              | implemented                                        |
| 1.1.1.4 Ensure mounting of squashfs filesystems is disabled (Scored)                             | implemented                                        |
| 1.1.1.5 Ensure mounting of udf filesystems is disabled (Scored)                                  | implemented                                        |
| 1.1.2 Ensure /tmp is configured (Scored)                                                         | not implemented                                    |
| 1.1.3 Ensure nodev option set on /tmp partition (Scored)                                         | not implemented                                    |
| 1.1.4 Ensure nosuid option set on /tmp partition (Scored)                                        | not implemented                                    |
| 1.1.4 Ensure nosuid option set on /tmp partition (Scored)                                        | not implemented                                    |
| 1.1.5 Ensure noexec option set on /tmp partition (Scored)                                        | not implemented                                    |
| 1.1.6 Ensure separate partition exists for /var (Scored)                                         | not implemented                                    |
| 1.1.7 Ensure separate partition exists for /var/tmp (Scored)                                     | not implemented                                    |
| 1.1.8 Ensure nodev option set on /var/tmp partition (Scored)                                     | not implemented                                    |
| 1.1.9 Ensure nosuid option set on /var/tmp partition (Scored)                                    | not implemented                                    |
| 1.1.10 Ensure noexec option set on /var/tmp partition (Scored)                                   | not implemented                                    |
| 1.1.11 Ensure separate partition exists for /var/log (Scored)                                    | not implemented                                    |
| 1.1.12 Ensure separate partition exists for /var/log/audit (Scored)                              | not implemented                                    |
| 1.1.13 Ensure separate partition exists for /home (Scored)                                       | not implemented                                    |
| 1.1.14 Ensure nodev option set on /home partition (Scored)                                       | not implemented                                    |
| 1.1.15 Ensure nodev option set on /dev/shm partition (Scored)                                    | implemented                                        |
| 1.1.16 Ensure nosuid option set on /dev/shm partition (Scored)                                   | included in 1.1.15                                 |
| 1.1.17 Ensure noexec option set on /dev/shm partition (Scored)                                   | included in 1.1.15                                 |
| 1.1.18 Ensure sticky bit is set on all world-writable directories (Scored)                       | implemented                                        |
| 1.1.19 Disable Automounting (Scored)                                                             | N/A (not installed on system defaults)             |
| 1.2 Configure Software Updates                                                                   |                                                    |
| 1.2.1 Ensure package manager repositories are configured (Not Scored)                            | N/A (already configured on system defaults)        |
| 1.2.2 Ensure GPG keys are configured (Not Scored)                                                | N/A (already configured on system defaults)        |
| 1.2.3 Ensure gpgcheck is globally activated (Scored)                                             | N/A (already configured on system defaults)        |
| 1.3 Filesystem Integrity Checking                                                                |                                                    |
| 1.3.1 Ensure AIDE is installed (Scored)                                                          | implemented                                        |
| 1.3.2 Ensure filesystem integrity is regularly checked (Scored)                                  | implemented                                        |
| 1.4 Secure Boot Settings                                                                         |                                                    |
| 1.4.1 Ensure permissions on bootloader config are configured (Scored)                            | implemented                                        |
| 1.4.2 Ensure authentication required for single user mode (Scored)                               | implemented                                        |
| 1.5 Additional Process Hardening                                                                 |                                                    |
| 1.5.1 Ensure core dumps are restricted (Scored)                                                  | implemented                                        |
| 1.5.2 Ensure address space layout randomization (ASLR) is enabled (Scored)                       | implemented                                        |
| 1.5.3 Ensure prelink is disabled (Scored)                                                        | N/A (already disabled on system defaults)          |
| 1.6 Mandatory Access Control                                                                     |                                                    |
| 1.6.1 Configure SELinux                                                                          | not implemented                                    |
| 1.6.1.1 Ensure SELinux is not disabled in bootloader configuration (Scored)                      | not implemented                                    |
| 1.6.1.2 Ensure the SELinux state is enforcing (Scored)                                           | not implemented                                    |
| 1.6.1.3 Ensure SELinux policy is configured (Scored)                                             | not implemented                                    |
| 1.6.1.4 Ensure SETroubleshoot is not installed (Scored)                                          | not implemented                                    |
| 1.6.1.5 Ensure the MCS Translation Service (mcstrans) is not installed (Scored)                  | not implemented                                    |
| 1.6.1.6 Ensure no unconfined daemons exist (Scored)                                              | not implemented                                    |
| 1.6.2 Ensure SELinux is installed (Scored)                                                       | not implemented                                    |
| 1.7 Warning Banners                                                                              |                                                    |
| 1.7.1 Command Line Warning Banners                                                               |                                                    |
| 1.7.1.1 Ensure message of the day is configured properly (Scored)                                | implemented                                        |
| 1.7.1.2 Ensure local login warning banner is configured properly (Not Scored)                    | implemented                                        |
| 1.7.1.3 Ensure remote login warning banner is configured properly (Not Scored)                   | implemented                                        |
| 1.7.1.4 Ensure permissions on /etc/motd are configured (Not Scored)                              | implemented                                        |
| 1.7.1.5 Ensure permissions on /etc/issue are configured (Scored)                                 | implemented                                        |
| 1.7.1.6 Ensure permissions on /etc/issue.net are configured (Not Scored)                         | implemented                                        |
| 1.8 Ensure updates, patches, and additional security software are installed (Scored)             | implemented                                        |
| 2 Services                                                                                       |                                                    |
| 2.1 Special Purpose Services                                                                     |                                                    |
| 2.1.1 Time Synchronization                                                                       |                                                    |
| 2.1.1.1 Ensure time synchronization is in use (Not Scored)                                       | N/A (already enabled on system defaults)           |
| 2.1.1.2 Ensure ntp is configured (Scored)                                                        | N/A (chrony is configured as time sync service)    |
| 2.1.1.3 Ensure chrony is configured (Scored)                                                     | N/A (already configured on system defaults)        |
| 2.1.2 Ensure X Window System is not installed (Scored)                                           | N/A (not installed on system defaults)             |
| 2.1.3 Ensure Avahi Server is not enabled (Scored)                                                | N/A (not installed on system defaults)             |
| 2.1.4 Ensure CUPS is not enabled (Scored)                                                        | N/A (not installed on system defaults)             |
| 2.1.5 Ensure DHCP Server is not enabled (Scored)                                                 | N/A (not installed on system defaults)             |
| 2.1.6 Ensure LDAP server is not enabled (Scored)                                                 | N/A (not installed on system defaults)             |
| 2.1.7 Ensure NFS and RPC are not enabled (Scored)                                                | implemented                                        |
| 2.1.8 Ensure DNS Server is not enabled (Scored)                                                  | N/A (not installed on system defaults)             |
| 2.1.9 Ensure FTP Server is not enabled (Scored)                                                  | N/A (not installed on system defaults)             |
| 2.1.10 Ensure HTTP server is not enabled (Scored)                                                | N/A (not installed on system defaults)             |
| 2.1.11 Ensure IMAP and POP3 server is not enabled (Scored)                                       | N/A (not installed on system defaults)             |
| 2.1.12 Ensure Samba is not enabled (Scored)                                                      | N/A (not installed on system defaults)             |
| 2.1.13 Ensure HTTP Proxy Server is not enabled (Scored)                                          | N/A (not installed on system defaults)             |
| 2.1.14 Ensure SNMP Server is not enabled (Scored)                                                | N/A (not installed on system defaults)             |
| 2.1.15 Ensure mail transfer agent is configured for local-only mode (Scored)                     | N/A (already configured on system defaults)        |
| 2.1.16 Ensure NIS Server is not enabled (Scored)                                                 | N/A (not installed on system defaults)             |
| 2.1.17 Ensure rsh server is not enabled (Scored)                                                 | N/A (not installed on system defaults)             |
| 2.1.18 Ensure telnet server is not enabled (Scored)                                              | N/A (not installed on system defaults)             |
| 2.1.19 Ensure tftp server is not enabled (Scored)                                                | N/A (not installed on system defaults)             |
| 2.1.20 Ensure rsync service is not enabled (Scored)                                              | N/A (already disabled on system defaults)          |
| 2.1.21 Ensure talk server is not enabled (Scored)                                                | N/A (not installed on system defaults)             |
| 2.2 Service Clients                                                                              |                                                    |
| 2.2.1 Ensure NIS Client is not installed (Scored)                                                | N/A (not installed on system defaults)             |
| 2.2.2 Ensure rsh client is not installed (Scored)                                                | N/A (not installed on system defaults)             |
| 2.2.3 Ensure talk client is not installed (Scored)                                               | N/A (not installed on system defaults)             |
| 2.2.4 Ensure telnet client is not installed (Scored)                                             | N/A (not installed on system defaults)             |
| 2.2.5 Ensure LDAP client is not installed (Scored)                                               | N/A (not installed on system defaults)             |
| 3 Network Configuration                                                                          |                                                    |
| 3.1 Network Parameters (Host Only)                                                               |                                                    |
| 3.1.1 Ensure IP forwarding is disabled (Scored)                                                  | implemented                                        |
| 3.1.2 Ensure packet redirect sending is disabled (Scored)                                        | implemented                                        |
| 3.2 Network Parameters (Host and Router)                                                         |                                                    |
| 3.2.1 Ensure source routed packets are not accepted (Scored)                                     | implemented                                        |
| 3.2.2 Ensure ICMP redirects are not accepted (Scored)                                            | implemented                                        |
| 3.2.3 Ensure secure ICMP redirects are not accepted (Scored)                                     | implemented                                        |
| 3.2.4 Ensure suspicious packets are logged (Scored)                                              | implemented                                        |
| 3.2.5 Ensure broadcast ICMP requests are ignored (Scored)                                        | implemented                                        |
| 3.2.6 Ensure bogus ICMP responses are ignored (Scored)                                           | implemented                                        |
| 3.2.7 Ensure Reverse Path Filtering is enabled (Scored)                                          | implemented                                        |
| 3.2.8 Ensure TCP SYN Cookies is enabled (Scored)                                                 | implemented                                        |
| 3.2.9 Ensure IPv6 router advertisements are not accepted (Scored)                                | implemented                                        |
| 3.3 TCP Wrappers                                                                                 |                                                    |
| 3.3.1 Ensure TCP Wrappers is installed (Scored)                                                  | N/A (already enabled on system defaults)           |
| 3.3.2 Ensure /etc/hosts.allow is configured (Not Scored)                                         | not implemented                                    |
| 3.3.3 Ensure /etc/hosts.deny is configured (Not Scored)                                          | not implemented                                    |
| 3.3.4 Ensure permissions on /etc/hosts.allow are configured (Scored)                             | implemented                                        |
| 3.3.5 Ensure permissions on /etc/hosts.deny are configured (Scored)                              | implemented                                        |
| 3.4 Uncommon Network Protocols                                                                   |                                                    |
| 3.4.1 Ensure DCCP is disabled (Not Scored)                                                       | implemented                                        |
| 3.4.2 Ensure SCTP is disabled (Not Scored)                                                       | implemented                                        |
| 3.4.3 Ensure RDS is disabled (Not Scored)                                                        | implemented                                        |
| 3.4.4 Ensure TIPC is disabled (Not Scored)                                                       | implemented                                        |
| 3.5 Firewall Configuration                                                                       |                                                    |
| 3.5.1 Configure IPv4 iptables                                                                    |                                                    |
| 3.5.1.1 Ensure default deny firewall policy (Scored)                                             | not implemented                                    |
| 3.5.1.2 Ensure loopback traffic is configured (Scored)                                           | not implemented                                    |
| 3.5.1.3 Ensure outbound and established connections are configured (Not Scored)                  | not implemented                                    |
| 3.5.1.4 Ensure firewall rules exist for all open ports (Scored)                                  | not implemented                                    |
| 3.5.2 Configure IPv6 ip6tables                                                                   |                                                    |
| 3.5.2.1 Ensure IPv6 default deny firewall policy (Scored)                                        | not implemented                                    |
| 3.5.2.2 Ensure IPv6 loopback traffic is configured (Scored)                                      | not implemented                                    |
| 3.5.2.3 Ensure IPv6 outbound and established connections are configured (Not Scored)             | not implemented                                    |
| 3.5.2.4 Ensure IPv6 firewall rules exist for all open ports (Not Scored)                         | not implemented                                    |
| 3.5.3 Ensure iptables is installed (Scored)                                                      | not implemented                                    |
| 3.6 Disable IPv6 (Not Scored)                                                                    | implemented                                        |
| 4 Logging and Auditing                                                                           |                                                    |
| 4.1 Configure System Accounting (auditd)                                                         |                                                    |
| 4.1.1 Configure Data Retention                                                                   |                                                    |
| 4.1.1.1 Ensure audit log storage size is configured (Not Scored)                                 | implemented                                        |
| 4.1.1.2 Ensure system is disabled when audit logs are full (Scored)                              | implemented                                        |
| 4.1.1.3 Ensure audit logs are not automatically deleted (Scored)                                 | implemented                                        |
| 4.1.2 Ensure auditd service is enabled (Scored)                                                  | N/A (already enabled on system defaults)           |
| 4.1.3 Ensure auditing for processes that start prior to auditd is enabled (Scored)               | included in 3.6                                    |
| 4.1.4 Ensure events that modify date and time information are collected (Scored)                 | implemented                                        |
| 4.1.5 Ensure events that modify user/group information are collected (Scored)                    | implemented                                        |
| 4.1.6 Ensure events that modify the system's network environment are collected (Scored)          | implemented                                        |
| 4.1.7 Ensure events that modify the system's Mandatory Access Controls are collected (Scored)    | implemented                                        |
| 4.1.8 Ensure login and logout events are collected (Scored)                                      | implemented                                        |
| 4.1.9 Ensure session initiation information is collected (Scored)                                | implemented                                        |
| 4.1.10 Ensure discretionary access control permission modification events are collected (Scored) | implemented                                        |
| 4.1.11 Ensure unsuccessful unauthorized file access attempts are collected (Scored)              | implemented                                        |
| 4.1.12 Ensure use of privileged commands is collected (Scored)                                   | implemented                                        |
| 4.1.13 Ensure successful file system mounts are collected (Scored)                               | implemented                                        |
| 4.1.14 Ensure file deletion events by users are collected (Scored)                               | implemented                                        |
| 4.1.15 Ensure changes to system administration scope (sudoers) is collected (Scored)             | implemented                                        |
| 4.1.16 Ensure system administrator actions (sudolog) are collected (Scored)                      | implemented                                        |
| 4.1.17 Ensure kernel module loading and unloading is collected (Scored)                          | implemented                                        |
| 4.1.18 Ensure the audit configuration is immutable (Scored)                                      | implemented                                        |
| 4.2 Configure Logging                                                                            |                                                    |
| 4.2.1 Configure rsyslog                                                                          |                                                    |
| 4.2.1.1 Ensure rsyslog Service is enabled (Scored)                                               | N/A (already enabled on system defaults)           |
| 4.2.1.2 Ensure logging is configured (Not Scored)                                                | N/A (already configured on system defaults)        |
| 4.2.1.3 Ensure rsyslog default file permissions configured (Scored)                              | implemented                                        |
| 4.2.1.4 Ensure rsyslog is configured to send logs to a remote log host (Scored)                  | N/A (already configured on system defaults)        |
| 4.2.1.5 Ensure remote rsyslog messages are only accepted on designated log hosts. (Not Scored)   | not implemented (cloudwatch configuration advised) |
| 4.2.2 Configure syslog-ng                                                                        |                                                    |
| 4.2.2.1 Ensure syslog-ng service is enabled (Scored)                                             | N/A (rsyslog is configured)                        |
| 4.2.2.2 Ensure logging is configured (Not Scored)                                                | N/A (rsyslog is configured)                        |
| 4.2.2.3 Ensure syslog-ng default file permissions configured (Scored)                            | N/A (rsyslog is configured)                        |
| 4.2.2.4 Ensure syslog-ng is configured to send logs to a remote log host (Not Scored)            | N/A (rsyslog is configured)                        |
| 4.2.2.5 Ensure remote syslog-ng messages are only accepted on designated log hosts (Not Scored)  | N/A (rsyslog is configured)                        |
| 4.2.3 Ensure rsyslog or syslog-ng is installed (Scored)                                          | N/A (already installed on system defaults)         |
| 4.2.4 Ensure permissions on all logfiles are configured (Scored)                                 | implemented                                        |
| 4.3 Ensure logrotate is configured (Not Scored)                                                  | N/A (already configured on system defaults)        |
| 5 Access, Authentication and Authorization                                                       |                                                    |
| 5.1 Configure cron                                                                               |                                                    |
| 5.1.1 Ensure cron daemon is enabled (Scored)                                                     | N/A (already enabled on system defaults)           |
| 5.1.2 Ensure permissions on /etc/crontab are configured (Scored)                                 | implemented                                        |
| 5.1.3 Ensure permissions on /etc/cron.hourly are configured (Scored)                             | implemented                                        |
| 5.1.4 Ensure permissions on /etc/cron.daily are configured (Scored)                              | implemented                                        |
| 5.1.5 Ensure permissions on /etc/cron.weekly are configured (Scored)                             | implemented                                        |
| 5.1.6 Ensure permissions on /etc/cron.monthly are configured (Scored)                            | implemented                                        |
| 5.1.7 Ensure permissions on /etc/cron.d are configured (Scored)                                  | implemented                                        |
| 5.1.8 Ensure at/cron is restricted to authorized users (Scored)                                  | implemented                                        |
| 5.2 SSH Server Configuration                                                                     |                                                    |
| 5.2.1 Ensure permissions on /etc/ssh/sshd_config are configured (Scored)                         | N/A (already configured on system defaults)        |
| 5.2.2 Ensure permissions on SSH private host key files are configured (Scored)                   | N/A (already configured on system defaults)        |
| 5.2.3 Ensure permissions on SSH public host key files are configured (Scored)                    | N/A (already configured on system defaults)        |
| 5.2.4 Ensure SSH Protocol is set to 2 (Scored)                                                   | implemented                                        |
| 5.2.5 Ensure SSH LogLevel is appropriate (Scored)                                                | implemented                                        |
| 5.2.6 Ensure SSH X11 forwarding is disabled (Scored)                                             | implemented                                        |
| 5.2.7 Ensure SSH MaxAuthTries is set to 4 or less (Scored)                                       | implemented                                        |
| 5.2.8 Ensure SSH IgnoreRhosts is enabled (Scored)                                                | implemented                                        |
| 5.2.9 Ensure SSH HostbasedAuthentication is disabled (Scored)                                    | implemented                                        |
| 5.2.10 Ensure SSH root login is disabled (Scored)                                                | implemented                                        |
| 5.2.11 Ensure SSH PermitEmptyPasswords is disabled (Scored)                                      | implemented                                        |
| 5.2.12 Ensure SSH PermitUserEnvironment is disabled (Scored)                                     | implemented                                        |
| 5.2.13 Ensure only strong ciphers are used (Scored)                                              | implemented                                        |
| 5.2.14 Ensure only strong MAC algorithms are used (Scored)                                       | implemented                                        |
| 5.2.15 Ensure that strong Key Exchange algorithms are used (Scored)                              | implemented                                        |
| 5.2.16 Ensure SSH Idle Timeout Interval is configured (Scored)                                   | implemented                                        |
| 5.2.17 Ensure SSH LoginGraceTime is set to one minute or less (Scored)                           | implemented                                        |
| 5.2.18 Ensure SSH access is limited (Scored)                                                     | not implemented                                    |
| 5.2.19 Ensure SSH warning banner is configured (Scored)                                          | implemented                                        |
| 5.3 Configure PAM                                                                                |                                                    |
| 5.3.1 Ensure password creation requirements are configured (Scored)                              | not implemented                                    |
| 5.3.2 Ensure lockout for failed password attempts is configured (Scored)                         | not implemented                                    |
| 5.3.3 Ensure password reuse is limited (Scored)                                                  | not implemented                                    |
| 5.3.4 Ensure password hashing algorithm is SHA-512 (Scored)                                      | not implemented                                    |
| 5.4 User Accounts and Environment                                                                |                                                    |
| 5.4.1 Set Shadow Password Suite Parameters                                                       |                                                    |
| 5.4.1.1 Ensure password expiration is 365 days or less (Scored)                                  | not implemented                                    |
| 5.4.1.2 Ensure minimum days between password changes is 7 or more (Scored)                       | not implemented                                    |
| 5.4.1.3 Ensure password expiration warning days is 7 or more (Scored)                            | not implemented                                    |
| 5.4.1.4 Ensure inactive password lock is 30 days or less (Scored)                                | not implemented                                    |
| 5.4.1.5 Ensure all users last password change date is in the past (Scored)                       | not implemented                                    |
| 5.4.2 Ensure system accounts are non-login (Scored)                                              | N/A (already configured on system defaults)        |
| 5.4.3 Ensure default group for the root account is GID 0 (Scored)                                | N/A (already configured on system defaults)        |
| 5.4.4 Ensure default user umask is 027 or more restrictive (Scored)                              | implemented                                        |
| 5.4.5 Ensure default user shell timeout is 900 seconds or less (Scored)                          | included in 5.4.4                                  |
| 5.5 Ensure root login is restricted to system console (Not Scored)                               | not implemented                                    |
| 5.6 Ensure access to the su command is restricted (Scored)                                       | not implemented                                    |
| 6 System Maintenance                                                                             |                                                    |
| 6.1 System File Permissions                                                                      |                                                    |
| 6.1.1 Audit system file permissions (Not Scored)                                                 | N/A (already configured on system defaults)        |
| 6.1.2 Ensure permissions on /etc/passwd are configured (Scored)                                  | N/A (already configured on system defaults)        |
| 6.1.3 Ensure permissions on /etc/shadow are configured (Scored)                                  | N/A (already configured on system defaults)        |
| 6.1.4 Ensure permissions on /etc/group are configured (Scored)                                   | N/A (already configured on system defaults)        |
| 6.1.5 Ensure permissions on /etc/gshadow are configured (Scored)                                 | N/A (already configured on system defaults)        |
| 6.1.6 Ensure permissions on /etc/passwd- are configured (Scored)                                 | N/A (already configured on system defaults)        |
| 6.1.7 Ensure permissions on /etc/shadow- are configured (Scored)                                 | N/A (already configured on system defaults)        |
| 6.1.8 Ensure permissions on /etc/group- are configured (Scored)                                  | N/A (already configured on system defaults)        |
| 6.1.9 Ensure permissions on /etc/gshadow- are configured (Scored)                                | N/A (already configured on system defaults)        |
| 6.1.10 Ensure no world writable files exist (Scored)                                             | N/A (already configured on system defaults)        |
| 6.1.11 Ensure no unowned files or directories exist (Scored)                                     | N/A (already configured on system defaults)        |
| 6.1.12 Ensure no ungrouped files or directories exist (Scored)                                   | N/A (already configured on system defaults)        |
| 6.1.13 Audit SUID executables (Not Scored)                                                       | N/A (already configured on system defaults)        |
| 6.1.14 Audit SGID executables (Not Scored)                                                       | N/A (already configured on system defaults)        |
| 6.2 User and Group Settings                                                                      |                                                    |
| 6.2.1 Ensure password fields are not empty (Scored)                                              | N/A (already configured on system defaults)        |
| 6.2.2 Ensure no legacy "+" entries exist in /etc/passwd (Scored)                                 | N/A (already configured on system defaults)        |
| 6.2.3 Ensure no legacy "+" entries exist in /etc/shadow (Scored)                                 | N/A (already configured on system defaults)        |
| 6.2.4 Ensure no legacy "+" entries exist in /etc/group (Scored)                                  | N/A (already configured on system defaults)        |
| 6.2.5 Ensure root is the only UID 0 account (Scored)                                             | N/A (already configured on system defaults)        |
| 6.2.6 Ensure root PATH Integrity (Scored)                                                        | N/A (already configured on system defaults)        |
| 6.2.7 Ensure all users' home directories exist (Scored)                                          | N/A (already configured on system defaults)        |
| 6.2.8 Ensure users' home directories permissions are 750 or more restrictive (Scored)            | N/A (already configured on system defaults)        |
| 6.2.9 Ensure users own their home directories (Scored)                                           | N/A (already configured on system defaults)        |
| 6.2.10 Ensure users' dot files are not group or world writable (Scored)                          | N/A (already configured on system defaults)        |
| 6.2.11 Ensure no users have .forward files (Scored)                                              | N/A (already configured on system defaults)        |
| 6.2.12 Ensure no users have .netrc files (Scored)                                                | N/A (already configured on system defaults)        |
| 6.2.13 Ensure users' .netrc Files are not group or world accessible (Scored)                     | N/A (already configured on system defaults)        |
| 6.2.14 Ensure no users have .rhosts files (Scored)                                               | N/A (already configured on system defaults)        |
| 6.2.15 Ensure all groups in /etc/passwd exist in /etc/group (Scored)                             | N/A (already configured on system defaults)        |
| 6.2.16 Ensure no duplicate UIDs exist (Scored)                                                   | N/A (already configured on system defaults)        |
| 6.2.17 Ensure no duplicate GIDs exist (Scored)                                                   | N/A (already configured on system defaults)        |
| 6.2.18 Ensure no duplicate user names exist (Scored)                                             | N/A (already configured on system defaults)        |
| 6.2.19 Ensure no duplicate group names exist (Scored)                                            | N/A (already configured on system defaults)        |

> Note that, this build component prepared based on remediation steps included in CIS Amazon Linux 2 Benchmark version 1.0.0. and don’t represent a complete security solution. Because these best practices might not be appropriate or sufficient for your environment, treat them as helpful considerations rather than prescriptions.
