# Router-on-a-Stick (ROAS) - Inter-VLAN Routing, Subnetting, and DHCP

This project demonstrates **Inter-VLAN Routing** using the **Router-on-a-Stick (ROAS)** method with **three VLANs**, all subnets derived from the `192.168.1.0/24` network, along with **DHCP** configuration on the router to automatically assign IP addresses to each VLAN.

---

## 📜 Overview

**ROAS (Router-on-a-Stick)** is a method of Inter-VLAN Routing where a single physical router interface carries multiple VLANs using **802.1Q trunking** and subinterfaces.

In this setup:
- **1 Router** (Layer 3 device for routing between VLANs & DHCP server)
- **2 Switches** (interconnected with trunk links)
- **3 VLANs** (Accounting, Sales, HR)
- Main network `192.168.1.0/24` is **subnetted** into **three /26 subnets**.

---

## VLAN & Subnetting Scheme

| VLAN ID | Department  | Network Address   | Subnet Mask       | IP Range               | Gateway          |
|---------|-------------|-------------------|-------------------|------------------------|------------------|
| 10      | Accounting  | 192.168.1.0       | 255.255.255.192   | 192.168.1.1 - 192.168.1.62  | 192.168.1.1     |
| 20      | Sales       | 192.168.1.64      | 255.255.255.192   | 192.168.1.65 - 192.168.1.126 | 192.168.1.65    |
| 30      | HR          | 192.168.1.128     | 255.255.255.192   | 192.168.1.129 - 192.168.1.190| 192.168.1.129   |

---
