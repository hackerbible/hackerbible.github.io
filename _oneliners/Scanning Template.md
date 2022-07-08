---
title: |
  Check whether a port is open on a range
description: |
  Use nmap to check whether a port is open on a range.

  Command Reference:

  	Network: 192.168.4.0/24

  	-n: never do DNS resolution
command: |
  nmap -vv 192.168.4.0/24 -n -p3389 | awk -F'[ /]' '/Discovered open port/{print $NF":"$4}'
items:
  - No_Creds
OS:
  - Linux
attack_types:
  - Scanning
references:
  - https://nmap.org/download.html
  - https://nmap.org/nsedoc/scripts/krb5-enum-users.html
---
