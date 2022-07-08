---
title: |
  Check for DC’s (LDAP) on a range
description: |
  Use nmap to check if DC's are present on a range with LDAP.

  Command Reference:

  	Network: 192.168.4.0/24

  	-n: never do DNS resolution
command: |
  nmap -vv 192.168.4.0/24 -n -p389,636 | awk -F'[ /]' '/Discovered open port/{print $NF":"$4}'
items:
  - No_Creds
services:
  - LDAP
OS:
  - Linux
attack_types:
  - Scanning
references:
  - https://nmap.org/download.html
  - https://nmap.org/nsedoc/scripts/krb5-enum-users.html
---
