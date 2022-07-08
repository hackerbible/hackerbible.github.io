---
title: |
  Find uncommon shares in vast Windows Domains
description: |
  The script FindUncommonShares.py is a Python equivalent of PowerView's Invoke-ShareFinder.ps1 allowing to quickly find uncommon shares in vast Windows Domains.

  Command Reference:

  	Target IP: 10.10.10.1

  	Attacker IP: 10.10.10.2

  	Domain: test.local

  	Username: test

  	Password: Welkom01!

command: |
  python3 FindUncommonShares.py -u 'test' -d 'TEST.local' -p 'Welkom01!' --dc-ip 10.10.10.1
items:
  - Password
  - Username
  - Hash
services:
  - SMB
OS:
  - Linux
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/p0dalirius/FindUncommonShares
---
