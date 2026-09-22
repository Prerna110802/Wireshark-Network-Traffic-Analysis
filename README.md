# Network Traffic Analysis & Suspicious Activity Detection Using Wireshark

## Overview

This project demonstrates network traffic capture and analysis using **Wireshark** in a controlled Kali Linux and Ubuntu virtual lab. Different types of traffic were generated and analyzed to understand normal communication and identify suspicious reconnaissance activity.

## Objectives

* Capture and analyze network packets using Wireshark
* Analyze ICMP, DNS, HTTP and TCP traffic
* Identify source/destination IPs and ports
* Analyze TCP flags and network conversations
* Detect Nmap SYN scan activity

## Lab Environment

* **Kali Linux:** Traffic generation and security testing
* **Ubuntu:** Target/monitored system
* **Wireshark:** Packet capture and analysis
* **Nmap:** Network reconnaissance testing
* **VMware:** Virtual lab environment

## Traffic Analyzed

### 1. ICMP Traffic

Used `ping` to generate ICMP packets and analyzed request/reply communication.

### 2. DNS Traffic

Used `nslookup` to generate DNS queries and inspected DNS request/response packets.

### 3. HTTP Traffic

Created a simple HTTP server on Ubuntu and analyzed TCP/HTTP communication from Kali.

### 4. Nmap SYN Scan

Performed a controlled SYN scan from Kali against the Ubuntu lab machine and analyzed SYN packets in Wireshark to identify reconnaissance activity.

## Wireshark Filters

```text
icmp
```

```text
dns
```

```text
tcp.port == 8080
```

```text
tcp.flags.syn == 1 && tcp.flags.ack == 0
```

## Investigation Process

1. Started packet capture on the Kali `eth0` interface.
2. Generated different types of network traffic.
3. Applied Wireshark display filters.
4. Examined IP addresses, ports and TCP flags.
5. Identified the Nmap SYN scan pattern.
6. Saved screenshots as investigation evidence.

## Evidence

* `01-wireshark-capture.jpeg`
* `02-icmp-analysis.jpeg`
* `03-dns-analysis.jpeg`
* `04-http-analysis.jpeg`
* `05-nmap-syn-scan.jpeg`

## SOC Analyst Skills Demonstrated

* Network packet analysis
* Protocol identification
* TCP/IP analysis
* Reconnaissance detection
* Wireshark filtering
* Security investigation and evidence collection

> **Disclaimer:** All traffic generation and scanning activities were performed against systems inside a private VMware lab for learning purposes.

