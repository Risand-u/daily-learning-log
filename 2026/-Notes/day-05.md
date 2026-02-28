# Day 5 — DNS Theory and Project
Date: February 28, 2026
Topic: DNS (Domain Name System)
Stage: Stage 1 — Beginner
Status: ✅ Completed

---

## What is DNS?
DNS stands for Domain Name System.
It is the phone book of the internet.
Converts website names to IP addresses.

You type:     google.com
DNS finds:    142.250.180.46
Browser goes: to that IP address

---

## Why Do We Need DNS?

Without DNS:
- Have to type 142.250.180.46 for Google
- Have to memorize IP for every website
- Very hard and confusing ❌

With DNS:
- Just type google.com
- DNS finds IP automatically
- Easy and fast ✅

---

## How DNS Works Step by Step

Step 1 → You type google.com in browser
Step 2 → Computer checks its own memory (cache)
         Already know IP? → go directly
         Dont know IP?   → ask DNS server
Step 3 → DNS server checks its records
         Finds google.com IP address
Step 4 → DNS tells computer the IP
Step 5 → Computer connects to that IP
         Website loads!

---

## Types of DNS Records

A Record
- Most common record
- Converts domain name to IP address
- google.com → 142.250.180.46

CNAME Record
- Nickname record
- Points one domain to another
- www.google.com → google.com

MX Record
- Mail record
- Tells where to send emails
- @google.com → mail.google.com

PTR Record
- Reverse record
- Converts IP back to domain name
- 142.250.180.46 → google.com

---

## DNS Hierarchy
Root (.)
    |
.com  .org  .net  .lk  .uk
    |
google.com  facebook.com
    |
mail.google.com  maps.google.com

---

## DNS Cache
Your computer remembers DNS answers to save time.

First visit:
Computer asks DNS → gets IP → saves it

Second visit:
Computer already knows IP → goes directly
Much faster!

---

## Forward vs Reverse DNS

Forward DNS
Name → IP address
google.com → 142.250.180.46
Used every day!

Reverse DNS
IP address → Name
142.250.180.46 → google.com
Used for security and troubleshooting

---

## DNS vs DHCP

DHCP → gives IP address automatically
DNS  → converts names to IP addresses

They work together:
DHCP gives PC an IP address
DHCP also tells PC which DNS server to use
DNS helps PC find websites by name

---

## What I Built in Packet Tracer

Network layout:
Router (2911)
      |
    Switch
   /      \
PC0       DNS Server
          192.168.1.50

DNS Records I Added:
company.com     → 192.168.1.50
www.company.com → 192.168.1.50

---

## Server Static IP
IP Address:      192.168.1.50
Subnet Mask:     255.255.255.192
Default Gateway: 192.168.1.1

Server always needs static IP
because it never changes!

---

## Commands I Used

# Tell router about DNS server
ip name-server 192.168.1.50

# Update DHCP pools with DNS server
ip dhcp pool IT-DEPARTMENT
dns-server 192.168.1.50

ip dhcp pool OFFICE-STAFF
dns-server 192.168.1.50

ip dhcp pool MANAGEMENT
dns-server 192.168.1.50

# Test DNS from PC
ping company.com
nslookup company.com

---

## Test Results
- DNS service turned on ✅
- DNS records added ✅
- PC0 pinged company.com successfully ✅
- nslookup showed correct IP ✅

---

## Simple Summary
DNS      = phone book of internet
Domain   = website name like google.com
IP       = actual address like 142.250.180.46
A Record = converts name to IP
Cache    = saved DNS answers for speed
Forward  = name to IP
Reverse  = IP to name
Server   = always needs static IP

---

## Struggles Today
- Had to find DNS service in Server settings
- Remembered to renew DHCP on PCs after
  updating DNS server IP

---


---

