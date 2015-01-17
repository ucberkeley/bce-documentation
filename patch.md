---
layout: default
title: Patching
---

Important: If there are any patch files associated with a given VM then after you import the VM into VirtualBox (or start an EC2 instance using the VM), you should copy the patch file to the VM, click on the Terminal Emulator icon, and then run the following at the command-line prompt:

    oski@BCE:~$ sudo source name_of_patch_file

