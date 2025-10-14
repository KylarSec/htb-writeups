# HTB Fawn Writeup

## Quick Summary
**Machine:** Fawn  
**Difficulty:** Very Easy  
**Platform:** HackTheBox  
**Date:** 15-10-2025  
**Author:** kylarsec

## Enumeration
**Ports Found:**
- 21 (FTP) - **Exploited**

## Exploitation
1. **FTP Connection:** `ftp 10.129.1.14`
2. **Anonymous Access:** Username `anonymous` with blank password
3. **File Listing:** `ls` revealed `flag.txt`
4. **File Download:** `get flag.txt` to retrieve the flag

## Key Learnings
- FTP anonymous authentication is a critical misconfiguration
- Different protocols require different client tools
- Understanding proper file transfer commands for each service
- Anonymous access often indicates poor security practices

## Remediation
- Disable anonymous FTP access
- Implement strong authentication
- Use SFTP/FTPS instead of plain FTP
- Regular security audits of service configurations

## Flag
035db21c881520061c53e0536e44f815
