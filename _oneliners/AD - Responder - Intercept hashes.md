---
title: |
  Intercept hashes with Responder
description: |
  Responder is a LLMNR, NBT-NS and MDNS poisoner, with built-in HTTP/SMB/MSSQL/FTP/LDAP rogue authentication server supporting NTLMv1/NTLMv2/LMv2, Extended Security NTLMSSP and Basic HTTP authentication.

  Command Reference:

  	Network: 192.168.4.0/24

  	-I: interface

    -v: increase verbosity.

    -d: enable answers for DHCP broadcast requests. This option will inject a WPAD server in the DHCP response.

    -w: start the WPAD rogue proxy server. Default value is false.

    -P: force NTLM (transparently)/Basic (prompt) authentication for the proxy. WPAD doesn't need to be ON. Default: False
command: |
  python Responder.py -I <interface> -v -d -w -P
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
  - https://github.com/lgandx/Responder
---
