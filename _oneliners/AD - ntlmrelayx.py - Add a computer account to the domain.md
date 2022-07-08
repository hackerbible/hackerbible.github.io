---
title: |
  Add a computer account to the domain
description: |
  This module performs the SMB Relay attacks originally discovered by cDc extended to many target protocols (SMB, MSSQL, LDAP, etc).
  It receives a list of targets and for every connection received it will choose the next target and try to relay the credentials. Also, if specified, it will first to try authenticate against the client connecting to us. Add a computer account to the domain (use ldap:// for insecure ldap) (SMB signing must be disabled).

  Command Reference:

  	Target: ldaps://<dc-ip>
command: |
  ntlmrelayx.py -t ldaps://<dc-ip> --add-computer
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
