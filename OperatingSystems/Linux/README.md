# 🛠️ DevOps Journey — 6 Month Mastery Plan

**Purpose**: To master Linux and DevOps from the ground up, with a bottom-up, system-first mindset — suitable for long-term career investment.

**Pace**: 6 days/week (minimum 2 hrs/day), Sundays off.

**Structure**:

* **Phases**: Conceptual grouping (use as GitHub Milestones)
* **Weeks**: Execution steps (use as GitHub Issues)
* **Books**:

  * *How Linux Works* (HLW) — for systems theory
  * *Linux in Action* (LiA) — for hands-on projects
  * `man` pages — for command fluency and deeper insight

---

## 🔧 Phase 1: Core Linux Foundations (Weeks 1–4)

### Week 1: Big Picture & CLI Mastery

* HLW: Ch.1 The Big Picture
* HLW: Ch.2 Basic Commands (1st half)
* Practice: `cd`, `ls`, `cp`, `mv`, `rm`, `cat`, `less`, `find`, `grep`, pipes, redirections
* GPT-generated exercises: directory traversal, recursive search

### Week 2: Devices and Filesystems + Command Line & Recursion Exercises

* HLW Chapter 3–4
* Practice: `mount`, `umount`, `df`, `du`, `lsblk`, `blkid`, `mkfs`, partitioning with `fdisk`/`parted`
* Explore `/dev`, `/sys`, `/proc`
* Linux in Action: Archive management
* GPT exercises

### Week 3: Boot and Init Systems

* HLW Chapter 5–6
* Learn BIOS vs UEFI, bootloaders (`GRUB`), kernel loading, `systemd`, `init`
* Tools: `systemctl`, `journalctl`, `dmesg`, `systemd-analyze`
* Practice: Inspect services, boot targets

### Week 4: User & System Configuration

* HLW Chapter 7
* Practice: `cron` jobs, timezone, system logging (`rsyslog`, `journalctl`)
* `man` pages: `crontab`, `logger`, `useradd`, `passwd`
* Linux in Action: Automating backups

---

## ⚙️ Phase 2: Processes, System Monitoring, and User Management (Weeks 5–8)

### Week 5: Process Management

* HLW Chapter 8
* Practice: `ps`, `top`, `htop`, `nice`, `renice`, `kill`, `strace`, `lsof`
* Visualize process trees, zombie/orphan states

### Week 6: Resource Utilization & Logs

* Linux in Action: System Monitoring, Log File Analysis
* Practice: `/proc`, `/sys`, memory maps, I/O usage
* Tools: `vmstat`, `iostat`, `iotop`, `free`, `uptime`, `sar`

### Week 7: User and Group Management

* Files: `/etc/passwd`, `/etc/shadow`, `/etc/group`
* Commands: `usermod`, `groupadd`, `id`, `who`, `groups`, `su`, `sudo`
* Practice secure user environments

### Week 8: Shell Scripting

* HLW Chapter 11
* Scripts: backups, logs cleanup, user reports
* Learn: `if`, `for`, `case`, functions, positional args
* Tools: `getopts`, `xargs`, `tee`, `cut`, `awk`, `sed`

---

## 🌐 Phase 3: Networking Fundamentals (Weeks 9–13)

### Week 9: Networking Internals

* HLW Chapter 9
* Commands: `ip a`, `ip r`, `netstat, ss`, `ping`, `traceroute`, `dig`
* Practice: Manual IP configs, `/etc/network/interfaces`, `resolv.conf`

### Week 10: Network Applications & Services

* HLW Chapter 10
* Practice with: `curl`, `wget`, `scp`, `rsync`, `ssh`, `nmap`, `nc`, `telnet`
* Deploy basic HTTP & FTP servers (`python -m http.server`, `vsftpd`)

### Week 11: Firewalls & Packet Filtering

* Deep-dive: `iptables`, `nftables`, `firewalld`
* Practice: create rules for `SSH`, `HTTP`, custom ports
* Use: `iptables-save`, `iptables-restore`

### Week 12: Week 12: VPN & DMZ

* Linux in Action: VPN/DMZ
* Tools: `ufw`, `fail2ban`, `iptables` for port forwarding
* Practice: setup `DMZ` with virtual machines or containers

### Week 13: Refresh Week

* LiA: VPN / DMZ chapter
* Practice: SSH tunnels, `autossh`, WireGuard/OpenVPN setup
* Grand Practice

---

## 📡 Phase 4: System Security & File Sharing (Weeks 14–17)

### Week 14: File Permissions and ACLs

* Deep dive: `chmod`, `chown`, `umask`, `setuid`, `setgid`, sticky bit
* Practice: ACLs with `getfacl`, `setfacl`
* Linux in Action: Secure your web server

### Week 15: Secure File Transfer & Sharing

* HLW Chapter 12, LIA Chapter: `Nextcloud`
* Practice: `Samba`, `NFS`, `SSHFS`
* Setup: user authentication, access control

### Week 16: Logs and Auditing

* Practice: log rotation (`logrotate`), `auditd`, `ausearch`, `journaling`
* Tools: `auditctl`, `last`, `wtmp`, `btmp`, `who`, `faillog`

### Week 17: Performance Profiling

* Tools: `perf`, `iotop`, `iotune`, `top`, `ps`, `vmstat`
* Detect slow services, optimize scripts
* Linux in Action: Performance troubleshooting

---

## 🧠 Phase 5: Web Services, Containers, and DevOps Tooling (Weeks 18–22)

### Week 18: Web Servers

* LIA Chapter: MediaWiki server
* Practice: Apache, Nginx basics, virtual hosts, SSL
* Tools: `curl`, `ss`, `certbot`, `ufw`, `systemd`

### Week 19: Containers and Virtualization

* HLW Chapter 17
* Tools: docker, podman, lxc, virt-manager
* Practice: Build custom containers, isolated environments

### Week 20: Automating with Ansible

* LiA: Final chapter
* Practice: YAML, playbooks, roles
* Write playbooks to automate user creation, service deployments
* Practice: roles, handlers, inventories
* Project: Recreate backup system with Ansible

### Week 21: CI/CD and Deployment Basics

* Concepts: Git, GitHub Actions, Docker builds, secrets
* Practice: docker-compose, build and push containers
* Optional: Jenkins or GitLab CI basics

### Week 22: Network Troubleshooting

* LiA: Network issues chapter
* Practice: `tcpdump`, `wireshark`, DNS failures, firewall misconfigs

---

### 📦 Phase 6: Final Projects & Mastery (Weeks 23–26)

### Week 23–24: Capstone Project 1 — Full-stack DevOps Stack

* Setup: Linux server + Web app + Nginx + Docker + Ansible + GitHub Actions
* Implement: firewall, users, monitoring, and logging

### Week 25: Capstone Project 2 — Secure Internal Services

* Deploy: VPN + file share + backup server
* Harden: firewall, SSH, fail2ban, audits

### Week 26: Final Review
* Review all scripts, commands, configs
* Create GitHub repo: notes, scripts, Ansible playbooks
* Polish: README, architecture diagrams, bash configs

---

## 🎯 Final Deliverables

* Daily journal in Markdown
* GitHub repo with week-based issues and notes
* Hands-on scripts, configs, and VMs backed up
* End-of-month review logs
* Final “My Linux Handbook” summary

---

Would you like a GitHub starter structure for this roadmap?
