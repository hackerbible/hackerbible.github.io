---
title: |
  Fast range scan (if you know the ranges)
description: |
  Use nmap to check whether a port is open on a range.

  Command Reference:

  	Example Network: 192.168.33.* or 172.16.18-26.0/12

  	-n: never do DNS resolution

  	-sn: ping scan
command: |
  nmap 192.168.33.* -n -sn -oG - | awk '/Up$/{print $2}'
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
