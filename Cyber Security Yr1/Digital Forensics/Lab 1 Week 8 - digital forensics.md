---
Date: 2023-11-21T02:21:00
Summary: FTK imager and DD tool
---
#  Learning FTK images and DD
---

#uwe #digital-forensics #year1 #lab
Table of contents >>> [[Digital Forensics]]
Next lab >>> [[Lab 2 Week 9 - digital forensics]]

## Kali imaginga
---
Issue with this task is that **depending on USB** it Linux may not be able to detect it. Remeber to find solution to this.

it lists all connected drives:
`sudo fdisk -l`  & `lsusb`
to install dd tool:
`sudo apt-get install dcfldd` 
example command to get the image hash from usb drive:
`sudo dcfldd if=/dev/sdb of=./USBimageKali/USBdrive.dd hash=md5,sha1 hashlog=./hashes1_0.txt`

## FTK imager
---
1. Be aware which device you select to image as it takes really long time to process it.
2. Next select the destination of where to store it.
3. The output must be in *dd* because encase supports it.
4. Image *fragment size to 0*
5. Image verification and successful report:
![[Pasted image 20231121022619.png]]
