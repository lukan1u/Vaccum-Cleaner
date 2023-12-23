---
Date: 2023-10-03T11:19:00
Summary: setting up visual studio code and azure cloud. Also this module is using GitLab as cloud storage for your code. Setting up SSH connection. Cool stuff
---
# C++
---
#settings #uwe #cplusplus
Table of contents >>> [[cplusplus]]
## Setting up SSH connection with azure UWE cloud
---
==***Disclaimer:***==
- When generating keys do not change their name otherwise it won't work for some reason. you should have `id-rsa.pub` key by default
- You do not need a passphrase if you don't want to constantly type it. It's basically like a password.

***Method:***
1.  using **windows terminal** or **cmd** generate SSH keys `ssh-keygen`  on your main machine and move them to .ssh folder in your `%USERPROFILE%` folder. if you didn't change directory when generating keys they will be at the bottom of your `%USERPROFILE%` folder.
2. login to UWE azure cloud using this `az ssh vm --ip csctcloud.uwe.ac.uk`
3. create folder in your user home folder create .ssh folder `mkdir .ssh` in your cloud
4. create file called `authorized_keys` within .ssh folder
5. copy public key text from main machine to your cloud machine and paste it to `authorized_keys` file
6.  Login ```ssh lukasz2.pazdro@live.uwe.ac.uk@csctcloud.uwe.ac.uk```

***Connect your text editor (VS code to azure UWE cloud)*:**
![[Pasted image 20231015155133.png]]
- Click on this red/blue status bar (depending on the theme the colour will be different)
- Click on `Connect to host`
	-  Click on `+ Add New SSH Host`
	-  Copy and paste this login: `ssh lukasz2.pazdro@live.uwe.ac.uk@csctcloud.uwe.ac.uk`

## Gitlab info
---
This is where all of work is being stored (change l2-pazdro to your uwe username):
https://gitlab.uwe.ac.uk/l2-pazdro

We use Gitlab made by uwe:
https://gitlab.uwe.ac.uk/
More info about the commands found [here]

