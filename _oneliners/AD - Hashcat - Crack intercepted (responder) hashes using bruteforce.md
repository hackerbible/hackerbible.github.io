---
title: |
  Crack intercepted (responder) hashes using brute force
description: |
  hashcat is the world's fastest and most advanced password recovery utility, supporting five unique modes of attack for over 300 highly-optimized hashing algorithms. bruteforce 4 chars (d = 0-9 l = a-z u = A-Z)

  Command Reference:

  	-m: hashcat mode 5600 (NetNTLMv2)

    --force: ignore warnings
command: |
  hashcat -m 5600 hashes.txt -a 3 -1 ?d?l?u ?1?1?1?1
items:
  - Hash
OS:
  - Linux
attack_types:
  - Cracking
references:
  - https://hashcat.net/hashcat/
  - https://github.com/hashcat/hashcat
---
