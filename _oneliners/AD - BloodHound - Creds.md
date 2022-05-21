---
title: |
  BloodHound Remote Ingestion Creds

description: |
  bloodhound-python is a Python based ingestor for BloodHound, based on Impacket. It allows you to remotely collect data for bloodhound by querying LDAP

  Command Reference:

  	Target IP: 10.10.10.1
    Username: test
    Password: Welkom01!
  	Domain: test.local
    
command: |
  bloodhound-python -u test -p Welkom01 -ns 10.10.10.1 -d test.local -c All
items:
  - Username
  - Password
services:
  - LDAP
attack_types:
  - Enumeration
OS:
  - Linux
  - Windows
references:
  - https://github.com/BloodHoundAD/BloodHound
  - https://github.com/fox-it/BloodHound.py
---
