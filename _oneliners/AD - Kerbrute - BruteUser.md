---
title: |
  Enumerate valid AD accounts through Kerberos Pre-Auth using bruteforce on an account
description: |
  ropnop's kerbrute bruteforces and enumerates valid Active Directory accounts through Kerberos Pre-Authentication. The following command will bruteforce an account against a list of provided passwords given a username.

  Command Reference:

  	Domain: test.local

  	Password List: passwords.txt

  	Username: test
command: |
  kerbrute bruteuser -d test.local passwords.txt test
items:
  - Username
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
