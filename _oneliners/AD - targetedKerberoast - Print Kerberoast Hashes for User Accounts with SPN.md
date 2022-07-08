---
title: |
  Print "kerberoast" hashes for user accounts that have a SPN set
description: |
  targetedKerberoast is a Python script that can, like many others (e.g. GetUserSPNs.py), print "kerberoast" hashes for user accounts that have a SPN set. This tool brings the following additional feature: for each user without SPNs, it tries to set one (abuse of a write permission on the servicePrincipalName attribute), print the "kerberoast" hash, and delete the temporary SPN set for that operation.

  Command Reference:

  	Target IP: 10.10.10.1

  	Attacker IP: 10.10.10.2

  	Domain: test.local

  	Username: test

  	Password: Welkom01!

command: |
  python3 targetedKerberoast.py -d test.local -u test -p Welkom01! --dc-ip 10.10.10.1
items:
  - Password
  - Username
services:
  - Kerberos
  - NTLM
OS:
  - Linux
attack_types:
  - Exploitation
references:
  - https://github.com/ShutdownRepo/targetedKerberoast
---
