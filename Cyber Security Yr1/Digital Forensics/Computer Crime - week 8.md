---
Date: 2023-11-16T13:49:00
Summary:
---
# DFOR process and Data representation
---
#uwe #digital-forensics #year1 
Table of contents >>> [[Digital Forensics]]
Previous page >>> [[Computer Crime - week 7]]
Next Page >>> [[Computer Crime - Week 9]]

## The evidence recovery process
1. Planning - Preparation
2. Collection - Preparation
3. Examination 
4. Analysis - Interpretation
5. Reporting - Documentation

**Collection** of data from a USB stick in a forensic manner (create a forensic image using write blocking devices to avoid changing/altering the evidence).Also it includes actual seizure of the devices. Dead forensics and alive forensics are different to each other. 

**Collection phase**
- Use write-blocking devices to help create a forensic image of a HDD  without changing the evidence
- Some forensics VMs have the auto mount option disabled so that you can mount your HDD using the read only, no exec option.
- EnCase (among the others) comes with its own software and hardware imaging solutions (plus a software-based write-blocking function)
**Order of vitality** (*OVV*)(alive) - logs, checking all the running apps, **RAM**!!!!!, cache.
- CPU, cache and register content
- Routing table, ARP cache process table, kernel statistics
- Memory
- Temporary file system/swap space
- Data on hard disk
- Remotely logged data
- Data contained on archival media

**Evidence recovery process** often includes using write -blockers (hardware and software) that copy exact state of disk onto another one. Mobile devices have their own devices such as **UFED 4PC** piece of software that copies all data from a mobile phone onto another device.

**Examination process**
- Identifies  evidence within the collected data
- Explains its origin and significance to the case.
-  This helps 

**The analysis Phase**
-