---
Date: 
Summary:
---
#  Learning FTK images and DD
---

#uwe #digital-forensics #year1 #lab
Table of contents >>> [[Digital Forensics]]

## Kali imaging
---
it lists all connected drives
`sudo fdisk -l` 

to install dd tool
`sudo apt-get install dcfldd` t

command to get the image hash from usb drive -
`sudo dcfldd if=/dev/sdb of=./USBimageKali/USBdrive.dd hash=md5,sha1 hashlog=./hashes1_0.txt`