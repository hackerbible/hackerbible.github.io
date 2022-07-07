---
title: |
  Execute powershell command on the target machine (Admin priv needed)
description: |
  "CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks." - https://github.com/byt3bl33d3r/CrackMapExec/wiki. This command will execute a powershell command on the target machine if the user has Administrator privileges. using "-x" will execute from cmd.

  Command Reference:

  	Target IP: 10.10.10.1

  	Username: test

  	Password: Welkom01!

command: |
  crackmapexec smb 10.10.10.1 -u 'test' -p 'Welkom01!' -X '$Host'
items:
  - Username
  - Password
services:
  - SMB
attack_types:
  - Exploitation
OS:
  - Linux
references:
  - https://github.com/byt3bl33d3r/CrackMapExec
  - https://github.com/byt3bl33d3r/CrackMapExec/wiki
---
