# Day 2 — Subnetting
Date: February 25, 2026
Topic: Subnetting
Stage: Stage 1 — Beginner
Status: ✅ Completed

---

## What I Did Today
- Learned what subnetting is theory and practice
- Built a 3 department company network in Packet Tracer
- Configured 3 router interfaces for each subnet
- Set IP addresses on 6 PCs across 3 departments
- Tested connectivity within and between departments

---

## What is an IP Address?
Every device on a network needs an IP address.
Think of it like a home address.
It tells other devices where to send data.

192.168.1.10

---

## What is a Subnet Mask?
Subnet mask tells the device which part of the IP 
address is the network and which part is the device.

IP Address:  192.168.1.10
Subnet Mask: 255.255.255.0

255.255.255 = Network part (street name)
0           = Device part (house number)

---

## What is Subnetting?
Subnetting is dividing one big network into smaller 
networks. Just like dividing a big building into 
separate floors for different departments.

Before Subnetting:
One big network → 192.168.1.0/24
Everyone is on the same network
254 devices all mixed together

After Subnetting:
192.168.1.0/26   → IT Department  (62 devices)
192.168.1.64/26  → Office Staff   (62 devices)
192.168.1.128/26 → Management     (62 devices)

---

## Why Do We Use Subnetting?
- Keeps network traffic organized
- More secure — departments cant access each other
- Easier to manage
- Used in every real company network

---

## CIDR Notation
The number after / tells you how big the network is.

/24 = 254 devices (big network)
/25 = 126 devices
/26 = 62 devices
/27 = 30 devices
/28 = 14 devices
/29 = 6 devices
/30 = 2 devices (used for router links)

Bigger number after / = smaller network!

---

## Subnet Mask Cheat Sheet
| CIDR | Subnet Mask | Usable Devices |
|------|-------------|----------------|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

---

## Important Terms

Network Address
First address of subnet, identifies the network
192.168.1.0 ← cannot be given to a device

Broadcast Address
Last address of subnet, sends message to all devices
192.168.1.63 ← cannot be given to a device

Usable IP Range
Addresses you can give to devices
192.168.1.1 to 192.168.1.62 ← these are usable

Default Gateway
Always the router, first usable IP
192.168.1.1 ← router gets this

---

## What I Built in Packet Tracer

IT Department → 192.168.1.0/26
Router IP     → 192.168.1.1
PC1           → 192.168.1.2
PC2           → 192.168.1.3

Office Staff  → 192.168.1.64/26
Router IP     → 192.168.1.65
PC3           → 192.168.1.66
PC4           → 192.168.1.67

Management    → 192.168.1.128/26
Router IP     → 192.168.1.129
PC5           → 192.168.1.130
PC6           → 192.168.1.131

---

## Router Commands I Used

# IT Department interface
int gig0/0
ip address 192.168.1.1 255.255.255.192
no shutdown

# Office Staff interface
int gig0/1
ip address 192.168.1.65 255.255.255.192
no shutdown

# Management interface
int gig0/2
ip address 192.168.1.129 255.255.255.192
no shutdown

# Verify all interfaces
show ip interface brief

---

## Why Switches Needed No Configuration
The router handles all routing between subnets.
Switches just pass data through automatically
like hallways in a building.

Switches only need configuration for:
- VLANs on specific ports (Stage 2)
- Port security (Stage 2)
- Spanning Tree Protocol (Stage 3)

---

## Simple Summary
IP Address  = home address of a device
Subnet Mask = tells which part is network, which is device
Subnetting  = dividing big network into smaller ones
/26         = 62 usable devices per subnet
Router      = connects all subnets together
Switch      = just passes data through automatically

---

## Struggles I Had
- None! Subnetting theory was clear
- Packet Tracer setup went smoothly

---

## Tomorrow I Want to Learn
DHCP — automatic IP assignment to devices

---
Next Topic: DHCP
Previous Topic: Day 1 — Network Security Lab
