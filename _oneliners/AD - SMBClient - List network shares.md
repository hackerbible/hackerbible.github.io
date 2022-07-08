---
title: |
  List all available shares using valid credentials
description: |
  Smbclient is a tool used to communicate with SMB servers. The following command will list out all available shares on the target server using valid credentials.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	User: test

  	Password: Welkom01!

command: |
  smbclient -L <ip> -U Guest
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
attack_types:
  - Enumeration
references:
  - https://www.samba.org/samba/docs/current/man-html/smbclient.1.html
---
