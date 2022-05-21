---
title: |
  Enumerate users with winrm using Crackmapexec
description: |
  "CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks." - https://github.com/byt3bl33d3r/CrackMapExec/wiki. This command will enumerate domain groups, local groups, logged on users, relative identifiers (RIDs), sessions, domain users, SMB shares/permissions, and get the domain password policy. 

  Command Reference:

  	Target IP: 10.10.10.1
    Usersfile: users.txt
    Password: Welkom01!

command: |
  crackmapexec winrm 10.10.10.1 -u users.txt -p 'Welkom01' --continue-on-success
items:
  - No_Creds
services:
  - SMB
attack_types:
  - Enumeration
OS:
  - Linux
references:
  - https://github.com/byt3bl33d3r/CrackMapExec
  - https://github.com/byt3bl33d3r/CrackMapExec/wiki
---
