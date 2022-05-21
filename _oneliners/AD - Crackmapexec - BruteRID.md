---
title: |
  Enumerate users with RID Bruteforce
description: |
  "CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks." - https://github.com/byt3bl33d3r/CrackMapExec/wiki. This command will enumerate domain groups, local groups, logged on users, relative identifiers (RIDs), sessions, domain users, SMB shares/permissions, and get the domain password policy. 

  Command Reference:

    DC IP: 10.10.10.1
    Username: test
    Password: Welkom01!
    Domain: test.local

command: |
  crackmapexec smb 10.10.10.1 -u test -p Welkom01! --rid-brute
items:
  - Username
  - Password
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
