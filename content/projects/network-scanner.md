---
title: "Network Scanner"
date: 2025-04-10
---

The **Network Scanner** is a Python-based project designed to scan a network for live devices, open ports, and vulnerabilities. The project uses a combination of **Scapy** and **Nmap** to gather information about devices and services on the network.

To start, you need to install the required libraries:

```bash
pip install scapy nmap
```

Here's an example of how to scan a network for live devices using Scapy:

```python
from scapy.all import ARP, Ether, srp

def scan_network(target_ip):
    arp_request = ARP(pdst=target_ip)
    broadcast = Ether(dst="ff:ff:ff:ff:ff:ff")
    arp_request_broadcast = broadcast/arp_request

    # Send the packet and receive the response
    answered_list = srp(arp_request_broadcast, timeout=1, verbose=False)[0]

    # Parse the response and print the results
    for element in answered_list:
        print(f"IP Address: {element[1].psrc}, MAC Address: {element[1].hwsrc}")

# Example usage
scan_network("192.168.1.1/24")

```

In addition to basic network scanning, the project can be extended to perform more advanced scans such as port scans and vulnerability assessments using Nmap. Here’s an example of using Nmap to check for open ports:

```python
import nmap

nm = nmap.PortScanner()

def scan_ports(target_ip):
    nm.scan(target_ip, '22-443')
    for host in nm.all_hosts():
        print(f"Host: {host}, Open Ports: {nm[host].all_tcp()}")

# Example usage
scan_ports("192.168.1.1")

```

This project is useful for network administrators to quickly identify devices and vulnerabilities in the network, and can be used for both small-scale and large-scale networks.