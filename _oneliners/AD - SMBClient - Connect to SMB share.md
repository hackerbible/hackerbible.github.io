---
title: |
  Connect to an SMB share using valid credentials
description: |
  Smbclient is a tool used to communicate with SMB servers. The following command will connect to an SMB share `C$` using valid credentials.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	SMB Share: C$

  	Username: test

  	Password: Welkom01!

command: |
  smbclient \\\\test.local\\C$ -I 10.10.10.1 -U test Welkom01!
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
  - https://www.madirish.net/59
---
