---
Date: 2023-11-21T20:19:00
Summary: hash values are important for verification and also time zone can have big impact on the case so be aware of these things
---
# Computer Crime
---

#digital-forensics #tyear1 #uwe
Table of contents >>> [[Digital Forensics]]
Previous page >>> [[Computer Crime - week 8]]
Next Page >>> [[Computer Crime - Week 10]]
# Hash values
sa1sha and md5 are useful hash methodologies used to verify files integrity. However nowdays it is recommended to use sha-256 as it is the most difficult hash braking methdology

to verify evidence:
![[Pasted image 20231123222253.png]]

## Evidence examination
•Though all cases are different (in some way) and may require different handling  approaches, it is certainly possible to outline a process for evidence analysis.
1. Ensure you know the time zone of the evidence
2. Recover lost files and folders
3. Validate file signatures
4. Run a hash analysis
5. Examine log and registry files
6. Examine recovered files and folders
7. Examine file metadata
8. Identify email and internet activity
9. Identify external storage
10. Identify unknown or suspicious programs (and identify hidden volumes)
11. TIME STAPS ARE ESSENTIAL SO PLEASE SET THEM CORRECTLY

## Evidence can be changed
- A suspect may attempt to hide frequently used and potentially  incriminating files by changing the file extension (often to .exe or.dll, etc.).
- Most recent file types have a standardised ‘signature’ - the first  few characters in the file (called the magic number).
- It is easy (and important) to scan for files where the extension and  signature do not match.
- https://www.garykessler.net/library/file_sigs.html magic numbers

## Logs
- Modern operating systems keep logs of logins and logouts,  applications that have run and errors that have occurred (Event  logs).
- If we examine these files we can identify unauthorised access (i.e.  someone logging in to a business computer at 2am) or the  execution of undesirable programs.