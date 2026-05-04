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
- Practice Bash scripting for support workflows

## Environment

- OS: Ubuntu Linux
- Shell: Bash
- Tools: `uptime`, `hostnamectl`, `df`, `free`, `systemctl`, `journalctl`, `ss`, `ufw`, `apt`

## Skills Demonstrated

- Bash scripting
- Linux system monitoring
- Support triage automation
- Disk and memory checks
- Service diagnostics
- Log review
- Package update awareness

## Script Checks

The script reports:

- Hostname and OS details
- System uptime
- Disk usage
- Memory usage
- Failed systemd services
- Listening ports
- UFW firewall status
- Recent system errors
- Available package updates

## How to Run

Clone the repository:

```bash
git clone https://github.com/michaeltucker24/ubuntu-health-check-script.git
cd ubuntu-health-check-script
