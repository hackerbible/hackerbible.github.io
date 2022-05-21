---
title: |
  BloodHound Remote Ingestion

description: |
  bloodhound-python is a Python based ingestor for BloodHound, based on Impacket. It allows you to remotely collect data for bloodhound by querying LDAP

  Command Reference:
  	Target IP: 10.10.10.1
  	Domain: test.local

command: |
  bloodhound-python -d test.local -ns 10.10.10.1 -c All
items:
  - No_Creds
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
