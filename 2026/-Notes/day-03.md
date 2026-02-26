# Day 3 — DHCP Theory
Date: February 26, 2026
Topic: DHCP (Dynamic Host Configuration Protocol)
Stage: Stage 1 — Beginner
Status: 📖 Learning

---

## What is DHCP?
DHCP stands for Dynamic Host Configuration Protocol.
It automatically gives IP addresses to devices when 
they join a network. Just like how your phone 
automatically gets an IP when you connect to WiFi.

---

## Why Do We Need DHCP?

Without DHCP:
- IT person manually types IP on every computer
- Takes hours for big companies
- Very easy to make mistakes

With DHCP:
- Every device automatically gets an IP address
- Takes seconds
- No mistakes!

---

## How DHCP Works — DORA Process

D — Discover
PC joins network and shouts:
"Is there a DHCP server? I need an IP address!"

O — Offer
DHCP server responds:
"Yes I am here! I can give you 192.168.1.10"

R — Request
PC replies:
"Yes please I want 192.168.1.10"

A — Acknowledge
DHCP server confirms:
"Done! 192.168.1.10 is yours now!"

---

## What Does DHCP Give to Devices?
DHCP gives 4 things automatically:

1. IP Address      → 192.168.1.10
2. Subnet Mask     → 255.255.255.0
3. Default Gateway → 192.168.1.1
4. DNS Server      → 8.8.8.8

---

## Important DHCP Terms

DHCP Pool
A range of IP addresses DHCP can give out.
Like a box of name tags for devices to take.

192.168.1.10 to 192.168.1.100 = pool range

DHCP Lease
IP address is not permanent.
Given for limited time like 24 hours.
Device renews lease or IP goes back to pool.

DHCP Exclusion
IP addresses DHCP should never give out.
Reserved for special devices like:
- Router    → 192.168.1.1 (always fixed)
- Server    → 192.168.1.2 (always fixed)
- Printer   → 192.168.1.3 (always fixed)

---

## DHCP vs Static IP

DHCP (Dynamic)
- Automatic
- Used for normal PCs, phones, laptops
- IP can change

Static IP
- Manual
- Used for routers, servers, printers
- IP never changes

Simple Rule:
Normal devices  → use DHCP
Important devices → use Static IP

---

## Where Does DHCP Server Live?

Option 1 — On the Router
- Router acts as DHCP server
- Most common in small offices and homes
- This is what we will do in Packet Tracer!

Option 2 — On a Dedicated Server
- Separate server handles DHCP
- Used in big companies
- More control and management

---

## Real Life Examples
- Home WiFi router    → gives DHCP to your phone
- Coffee shop WiFi    → gives DHCP to your laptop
- Company network     → gives DHCP to employee computers
- School network      → gives DHCP to student devices

---

## Commands I Will Use in Packet Tracer

# Create DHCP pool
ip dhcp pool IT-DEPARTMENT

# Set network range
network 192.168.1.0 255.255.255.192

# Set default gateway
default-router 192.168.1.1

# Set DNS server
dns-server 8.8.8.8

# Exclude addresses for router and servers
ip dhcp excluded-address 192.168.1.1 192.168.1.10

---

## What I Will Build in Packet Tracer
Router as DHCP server with 3 pools:

IT Department pool   → 192.168.1.11 to 192.168.1.62
Office Staff pool    → 192.168.1.75 to 192.168.1.126
Management pool      → 192.168.1.139 to 192.168.1.190

PCs will automatically get IP addresses
without manually typing anything!

---

## Simple Summary
DHCP     = automatic IP address giver
DORA     = Discover, Offer, Request, Acknowledge
Pool     = range of IPs DHCP can give out
Lease    = how long device keeps the IP
Exclusion = IPs DHCP should never give out
Static   = manual IP for routers and servers
Dynamic  = automatic IP for normal devices

---

## Struggles Today
- None! Theory was easy to understand

---

## Tomorrow
Practice DHCP in Packet Tracer and build
the 3 department network with automatic IPs

---
Next Topic: DHCP Practice in Packet Tracer
Previous Topic: Day 2 — Subnetting
