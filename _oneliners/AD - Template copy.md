---
title: |
  Find active IP's on local network
description: |
  Use nmap to scan for all hosts that are up on a network.

  Command Reference:

  	Network: 172.16.0.0/12

  	-n: never do DNS resolution

  	-sn: ping scan
command: |
  nmap 172.16.0.0/12 -n -sn -oG - | awk '/Up$/{print $2}'
items:
  - No_Creds
services:
  - Enumeration
OS:
  - Linux
attack_types:
  - Enumeration
references:
  - https://nmap.org/download.html
  - https://nmap.org/nsedoc/scripts/krb5-enum-users.html
---
