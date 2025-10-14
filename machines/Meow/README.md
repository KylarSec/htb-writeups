# HTB Meow Writeup

## Quick Summary
**Machine:** Meow  
**Difficulty:** Easy  
**Platform:** HackTheBox  
**Date:** 15/10/2025  
**Author:** kylarsec

## Solution
1. **Enumeration:** Found port 23/telnet open
2. **Exploitation:** Connected via telnet and accessed with root/blank credentials
3. **Post-Exploitation:** Found flag at /root/flag.txt

## Key Learnings
- Always test default credentials
- Telnet without authentication is critical
- Simple misconfigurations can lead to full compromise

## Flag
b40abdfe23665f766f9c61ecba8a4c19
