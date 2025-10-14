# HTB Dancing Writeup

## Quick Summary
**Machine:** Dancing  
**Difficulty:** very Easy  
**Platform:** HackTheBox  
**Date:** 15-10-2025 
**Author:** kylarsec

## Enumeration
**Ports Found:**
- 135 (RPC)
- 139 (NetBIOS)
- 445 (SMB) - **Exploited**
- 5985 (WinRM)

## Exploitation
1. **SMB Enumeration:** `smbclient -L 10.129.1.12`
2. **Anonymous Access:** Successful with blank credentials
3. **Share Discovery:** Found `WorkShares` share
4. **Data Access:** Connected via `smbclient //10.129.1.12/WorkShares -U anonymous`
5. **Flag Extraction:** Found in `./James.P/flag.txt`

## Key Learnings
- SMB anonymous access is a common misconfiguration
- Network shares often contain sensitive information
- Always enumerate SMB shares during penetration tests
- Principle of Least Privilege should be applied to shares

## Remediation
- Disable SMB anonymous access
- Implement proper share permissions
- Require authentication for all network shares

## Flag
5f61c10dffbc77a704d76016a22f1664
