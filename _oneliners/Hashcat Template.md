---
title: |
  Crack intercepted (responder) hashes
description: |
  hashcat is the world's fastest and most advanced password recovery utility, supporting five unique modes of attack for over 300 highly-optimized hashing algorithms. 

  Command Reference:

  	-m: hashcat mode 5600 (NetNTLMv2)

    --force: ignore warnings
command: |
  hashcat -m 5600 hashes.txt wordlist.txt -o cracked.txt --force
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
