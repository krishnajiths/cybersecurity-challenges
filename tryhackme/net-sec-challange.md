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
‘’’bash
nmap -p <port-range> <target-ip>

### Version Scan
‘’’bash
nmap -sV -p <port-range> <target-ip>

### Read SSH Server Headers
‘’’bash
telnet <target-ip> <target-port>
