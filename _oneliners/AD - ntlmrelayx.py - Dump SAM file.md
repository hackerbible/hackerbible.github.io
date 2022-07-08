---
title: |
  Dump SAM file
description: |
  This module performs the SMB Relay attacks originally discovered by cDc extended to many target protocols (SMB, MSSQL, LDAP, etc).
  It receives a list of targets and for every connection received it will choose the next target and try to relay the credentials. Also, if specified, it will first to try authenticate against the client connecting to us.

  Command Reference:

  	-tf: targets file
command: |
  ntlmrelayx.py -tf targets.txt
items:
  - No_Creds
services:
  - SMB
  - LDAP
OS:
  - Linux
attack_types:
  - Enumeration
  - Exploitation
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/ntlmrelayx.py
---
