---
title: |
  Create a list of targets with SMB Signing disabled (required to relay)
description: |
  "CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks." - https://github.com/byt3bl33d3r/CrackMapExec/wiki. This command will enumerate domain groups, local groups, logged on users, relative identifiers (RIDs), sessions, domain users, SMB shares/permissions, and get the domain password policy. Create a list of targets with SMB Signing disabled (required to relay).

  Command Reference:

  	Target: 192.168.1.0/24
command: |
  crackmapexec smb 192.168.1.0/24 --gen-relay-list targets.txt
items:
  - No_Creds
services:
  - SMB
OS:
  - Linux
attack_types:
  - Enumeration
references:
  - https://github.com/byt3bl33d3r/CrackMapExec
  - https://github.com/byt3bl33d3r/CrackMapExec/wiki
---
