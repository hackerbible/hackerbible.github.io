---
title: |
  Find active IP's on local network
description: |
  Use masscan to scan for all hosts that are up on a network.

  Command Reference:

  	-iL: File with IP ranges to scan

  	-p: ports

  	-oL: output file name 
command: |
  masscan -iL ranges.txt --open --rate 60000 -p22,3389,80,443,445,8080 -oL up_ranges.txt
  cat up_ranges.txt | awk '{print $4}
items:
  - No_Creds
OS:
  - Linux
attack_types:
  - Scanning
references:
  - https://nmap.org/download.html
  - https://nmap.org/nsedoc/scripts/krb5-enum-users.html
---
