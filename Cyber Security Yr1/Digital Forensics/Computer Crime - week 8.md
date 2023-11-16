---
Date: 2023-11-16T13:49:00
Summary: evidence collection (dead and alive). live acquisition is the most preferable way to get access to data. Different types of forensics such as cloud or mobile.
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

**Order of vitality** (*OVV*)(*alive*) - logs, checking all the running apps, **RAM**!!!!!, cache.
- CPU, cache and register content
- Routing table, ARP cache process table, kernel statistics
- Memory
- Temporary file system/swap space
- Data on hard disk
- Remotely logged data
- Data contained on archival media

**Dead computer forensics**
- We take out the HDD from the device
- You take only image of writeable space (also be aware of bad sector which might be picked up by the software)
- Is the image exactly the same as the original evidence (no because it contains additional header information required for this case)

**Evidence recovery process** often includes using write -blockers (hardware and software) that copy exact state of disk onto another one. Mobile devices have their own devices such as **UFED 4PC** piece of software that copies all data from a mobile phone onto another device.

**Examination process**
- Identifies  evidence within the collected data
- Explains its origin and significance to the case.
-  This helps 

**The analysis Phase**
- Can also be considered as part of the examination process
- It looks at the product of the examination for its significance and value to the case
- Examination is a technical review that is the province of the forensic practitioner while analysis may be conducted by a range of people

**The report**
- The report outlines the examination process and the pertinent data revolvered and completes an examination. (witness statement)
- Examination notes must be preserved for disclosure or testimony purposes

## Data representation
Data is represented by hex, binary etc. In binary 2 bits give us 4 different values. 3bit can give us 8 different values. 4 bits can give us 16 different values.
- Half a bit is a **nibble**
![[Pasted image 20231116160609.png]]

**ASCII**  - American standard for coding for information interchange

**Endianness** (little endian, big endian) - meaning how you interpret the data. **Little endian** means that the low-order bye of the number is stored in memory at the lowest address and the high-order byte at the highest address. (the little end comes first) **Big endian** is the opposite of the little endian.
- Intel CPU use little endian byte order
- Macs use big endian byte order
![[Pasted image 20231116161601.png]]


*Cyberchef is useful for capture the flag
Encase will decode file information if needed* 
