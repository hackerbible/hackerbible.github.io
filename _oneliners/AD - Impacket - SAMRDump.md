---
title: |
  List system user acounts, available resource shares, and other sensitive information
description: |
  Impacket's samrdump.py communicates with the Security Account Manager Remote (SAMR) interface to list system user accounts, available resource shares, and other sensitive information.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: test

  	Password: Welkom01!

command: |
  python3 samrdump.py test.local/test:Welkom01!@10.10.10.1
items:
  - Password
  - Username
services:
  - RPC
OS:
  - Linux
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/samrdump.py
  - https://www.hackingarticles.in/impacket-guide-smb-msrpc/
---
