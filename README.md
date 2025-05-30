# Task-4: Setup and Use a Firewall on Windows/Linux

## Objective
To configure and test basic firewall rules to allow or block network traffic using:
- Windows Firewall (GUI or PowerShell)
- UFW (Uncomplicated Firewall) on Linux

## Tools Used
- Linux (Ubuntu 22.04) with UFW
- Windows 10 Firewall

## Steps Performed
1. Installed UFW (Uncomplicated Firewall)
```bash
sudo apt update
sudo apt install ufw
```
2. Enabled the Firewall
```bash
sudo ufw enable
```
3. Checked Current Firewall Status
```bash
sudo ufw status verbose
```
4. Blocked Inbound Traffic on Port 23 (Telnet)
```bash
sudo ufw deny 23
```
5. Tested Telnet Block
Installed Telnet:
```bash
sudo apt install telnet
```
Verified block:
```bash
telnet 192.168.11.141 23
```
6. Allowed SSH (Port 22) to Ensure Remote Access
```bash
sudo ufw allow 22
```
7. Tested SSH Access
Checked SSH service:
```bash
sudo systemctl status ssh
```
Verified SSH locally:
```bash
ssh localhost
```
8. Deleted the Telnet Block Rule (Restored State)
```bash
sudo ufw delete deny 23
```
9. Listed All Active Firewall Rules
```bash
sudo ufw status numbered
```
