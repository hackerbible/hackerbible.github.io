---
title: |
  Enumerate a list of SMB hosts for accessible SMB shares, both local and mapped drives
description: |
  SMBMap is a tool used to enumerate SMB share drives, including listing share drive permissions, share contents, upload/download functionality, file name enumeration, and remote command execution. The following command will enumerate a list of SMB hosts for accessible SMB shares, both local and mapped drives, using valid credentials.

  Command Reference:

  	Domain: test.local

  	SMB Hosts: smb-hosts.txt

  	Username: test

  	Password: Welkom01!

command: |
  python3 smbmap.py --host-file smb-hosts.txt -u test -p 'Welkom01!' -d test.local -L
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/ShawnDEvans/smbmap
  - https://www.nopsec.com/blog/smbmap-wield-it-like-the-creator/
---
