# Net Sec Challenge

## Overview
This challenge focused on basic network enumeration and service analysis using common cybersecurity tools.

# Tools Used
- Nmap
- Telnet
- Hydra

# Tasks Completed
- Identified open ports on the target machine
- Scanned for what version the open port is on
- Identify hidden messages within server headers
- Scanned for ports using FTP

# Example Commands

### Open port identification
```bash
# Searches for open ports in this range 
nmap -p <port-range> <target-ip>
```

### Version Scan
```bash
# Searches for open ports and also displays their service version
nmap -sV -p <port-range> <target-ip>
```

### Read SSH Server Headers
```bash
# Connects to the target ip at the target port and displays the ssh server header
telnet <target-ip> <target-port>
```

### Hydra Bruteforce onto users
```bash
# -t 8  -> Uses 8 parallel threads/tasks (increases speed)
# -vV   -> Verbose output showing every login attempt
# -L    -> File containing usernames
# -P    -> Password wordlist being used
# ftp:// -> Targets the FTP service

hydra -t 8 -vV -L <user-list>.txt -P /usr/share/wordlists/rockyou.txt ftp://<target-ip>:<target-port>
```
