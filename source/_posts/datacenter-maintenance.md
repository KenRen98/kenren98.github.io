---
title: DataCenter Design and Maintenance
date: 2021-10-20 17:22:17
tags:
  - server
  - proxmox
  - datacenter
  - VM
  - Docker
  - Networking
  - VLAN
  - SDWAN
  - HA
cover_detail: /2021/10/20/datacenter-maintenance/1.png
cover_index: /2021/10/20/datacenter-maintenance/450.png
---
Currently, we are running 3 DataCenters with more than 20 Server Nodes, 8 of which are currently imported to Pterodactyl. Each node utilizes Proxmox LXC + Docker to provide the Wings Backend, while the Front End is hosted in our main DataCenter. The remaining nodes are used to host various services or have been rented out for purposes such as WebHosting, Dedicated High-Performance Servers, MySQL/MariaDB, or Testing.

![GUI](3.jpg)
![GUI](2.jpg)
![GUI](1.jpg)

### Network Isolation and Security
VLAN is implemented to isolate VM data and Host data, ensuring a secure environment. VMs are properly configured with network policies, limiting data exchange between VM networks. We utilize pfsense as an Intrusion Detection System (IDS) and Intrusion Prevention System (IPS). With the help of snort, we actively prevent DoS and DDoS attacks, as well as other potential threats and data leaks.

### Backup and Recovery
A comprehensive backup plan and policies are in place to ensure that snapshots are generated periodically. This approach guarantees data recovery and disaster recovery capabilities, providing peace of mind and minimizing potential downtime.

### High Availability and Storage
Ceph is employed for High Availability (HA) reasons, ensuring that services remain accessible even in the event of hardware failure. Additionally, NAS is utilized as expandable storage and central backup storage, offering flexibility and robust data protection.

By integrating these technologies and practices, we maintain a resilient and efficient DataCenter infrastructure, capable of meeting diverse needs and maintaining the highest standards of performance and security.
