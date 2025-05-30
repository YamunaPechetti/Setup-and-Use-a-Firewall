# Task-4: Setup and Use a Firewall on Windows/Linux

## Objective
To configure and test basic firewall rules to allow or block network traffic using:
- Windows Firewall (GUI or PowerShell)
- UFW (Uncomplicated Firewall) on Linux

## Tools Used
- Linux (Ubuntu 22.04) with UFW
- Windows 10 Firewall

## Steps Performed
1. Checked current firewall status:
```bash
sudo ufw status verbose
```
2 Enabled the firewall:
```bash
sudo ufw enable
```
3. Blocked inbound traffic on port 23 (Telnet):
```bash
sudo ufw deny 23
```
4. Tested connectivity to port 23 using telnet localhost 23 (connection refused, as expected).
5. Allowed SSH to ensure remote access was maintained:
```bash
sudo ufw allow 22
```
5. Removed test rule to restore original state:
```bash
sudo ufw delete deny 23
```
6. Listed all rules:
```bash
sudo ufw status numbered
```
