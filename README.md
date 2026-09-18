# My-NetworkWalks-WK2-PM5-Network-Scanning-with-Zenmap

## Project: Network Scanning with Zenmap

This project focuses on performing network scanning using Zenmap (the official GUI version of Nmap) to discover live hosts, their IP addresses, and MAC addresses inside a virtual lab environment.

## Project Overview

In this project, I used Zenmap to scan the virtual network (10.0.0.0/24) and identify all active devices. The main objective was to learn how to perform network discovery, detect live hosts, and collect important information such as IP addresses and MAC addresses using a graphical scanning tool.

This lab is part of the Cybersecurity & Ethical Hacking course at Networkwalks.

## Objectives of this Project

- Download and install Zenmap on Windows PC.
- Find the local IP address and LAN subnet.
- Perform a network scan using Zenmap.
- Identify the number of live hosts in the subnet.
- Collect IP addresses of all live hosts.
- Collect MAC addresses of all live hosts.
- Document the scanning process and results.

## Lab Configuration

| Components           | Configuration                  |
|----------------------|--------------------------------|
| Host OS              | Windows 10                     |
| Scanner Machine      | Windows 10 VM                  |
| Target Machines      | Kali Linux + Windows 10 VM     |
| Scanning Tool        | Zenmap (Nmap GUI)              |
| Network Type         | NAT Network                    |
| Subnet Scanned       | 10.0.0.0/24                    |
| Kali Linux IP        | 10.0.0.2                       |
| Windows 10 VM IP     | 10.0.0.10                      |
| Gateway              | 10.0.0.1                       |

## Network Architecture

VirtualBox NAT Network (10.0.0.0/24)
├── 10.0.0.1 → Gateway
├── 10.0.0.2 → Kali Linux
└── 10.0.0.10 → Windows 10 VM (Scanner)

## Lab Setup Procedure

**Step 1 → Install Zenmap**  
Downloaded and installed Zenmap from the official Nmap website on the Windows 10 virtual machine.

**Step 2 → Find Local IP & Subnet**  
Used the `ipconfig` command to find the local IP address and determine the correct subnet for scanning.

**Step 3 → Perform Network Scan**  
Opened Zenmap and ran a **Ping Scan** on the subnet `10.0.0.0/24`.

**Step 4 → Analyze Results**  
Collected the list of live hosts, their IP addresses, and MAC addresses from the scan output.

**Step 5 → Document Findings**  
Recorded the number of live hosts and their details for the lab report.

## Lab Verification

| Test                           | Result                                      |
|--------------------------------|---------------------------------------------|
| Total Live Hosts               | 3 hosts up                                  |
| Live IP Addresses              | 10.0.0.1, 10.0.0.2, 10.0.0.10               |
| MAC Address (10.0.0.1)         | 52:55:0A:00:00:01                           |
| MAC Address (10.0.0.2)         | 08:00:27:95:64:47                           |
| MAC Address (10.0.0.10)        | 08-00-27-2D-CA-E1                           |

## Problems Encountered & Solutions

**Problem 1 — Zenmap Crashed**  
Issue: Zenmap became unresponsive while generating topology.  
Solution: Skipped Task 7 (Topology PDF) as it was not mandatory.

**Problem 2 — MAC Address Missing**  
Issue: One host’s MAC address was not visible in Zenmap.  
Solution: Used `ipconfig /all` command to retrieve the missing MAC address.

## What I Learned

- How to use Zenmap for network discovery.
- Difference between IP address and MAC address.
- How to perform and analyze Ping Scan results.
- How to extract MAC addresses using both Zenmap and Windows commands.
- Importance of proper documentation during scanning.

## Security & Ethical Use

All scanning activities were performed strictly inside an isolated virtual lab environment for educational purposes only.

## Tools & Resources

- Zenmap / Nmap: https://nmap.org/download.html
- VirtualBox: https://www.virtualbox.org

## Author

**Sagar Shah**  
Program: Cybersecurity at Networkwalks  
Week: 02 | Project Module: PM5 — Network Scanning with Zenmap
