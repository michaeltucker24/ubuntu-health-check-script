# Ubuntu Health Check Script

## Overview

This project contains a Bash script that collects basic Ubuntu system health information for initial troubleshooting and support triage.

The script checks system uptime, disk usage, memory usage, failed systemd services, listening ports, firewall status, recent system errors, and available package updates.

## Scenario

A support engineer receives a report that an Ubuntu server may be running slowly or experiencing service issues. Before performing deeper troubleshooting, the engineer needs a quick system health snapshot.

## Objectives

- Automate basic Linux health checks
- Collect system information quickly
- Identify failed services
- Review disk and memory usage
- Check open listening ports
- Review firewall status
- Display recent system errors
- Check available package updates
- Practice Bash scripting for support workflows

## Environment

- OS: Ubuntu Linux
- Shell: Bash
- Tools: `hostnamectl`, `uptime`, `df`, `free`, `systemctl`, `journalctl`, `ss`, `ufw`, `apt`

## Skills Demonstrated

- Bash scripting
- Linux system monitoring
- Support triage automation
- Disk and memory checks
- Service diagnostics
- Log review
- Firewall status review
- Package update awareness

## Script Checks

The script reports:

- Hostname and OS details
- Current user
- System uptime
- Disk usage
- Memory usage
- Failed systemd services
- Listening ports
- UFW firewall status
- Recent high-priority journal errors
- Available package updates

## How to Run

Clone the repository:

```bash
git clone https://github.com/michaeltucker24/ubuntu-health-check-script.git
cd ubuntu-health-check-script
```

Make the script executable:

```bash
chmod +x ubuntu-health-check.sh
```

Run the script:

```bash
./ubuntu-health-check.sh
```

## Example Commands Used

```bash
hostnamectl
whoami
uptime
df -h
free -h
systemctl --failed
journalctl -p 3 -xb
ss -tuln
sudo ufw status verbose
apt list --upgradable
```

## Sample Output

A sample output file is included in this repository:

```text
sample-output.txt
```

## Support Use Case

This script can be used during initial support triage to collect a quick system health snapshot before deeper investigation.

It is useful for identifying obvious issues such as high disk usage, low memory, failed services, missing firewall visibility, recent system errors, or pending package updates.

## Limitations

This script is designed for basic triage only. It does not replace deeper troubleshooting, service-specific log review, application monitoring, or production-grade observability tools.

## Lessons Learned

This project reinforced how Bash automation can reduce repetitive checks and improve the speed of initial Linux support investigations.

## Portfolio Note

This project is part of my Linux Support Engineer portfolio. It demonstrates practical troubleshooting, automation, and systems administration skills relevant to Ubuntu/Linux support roles.
