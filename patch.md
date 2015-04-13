---
layout: default
title: Patching
---

Important: If there are any patch files or add-on scripts associated with a given VM then after you import the VM into VirtualBox (or start an EC2 instance using the VM), you should copy the patch file/add-on script to the VM, click on the Terminal Emulator icon, and then run the following at the command-line prompt, substituting the name of the specific file/script in place of <name_of_patch_file>:

    oski@BCE:~$ sudo bash <name_of_patch_file> ; exec bash

The same instructions apply to use any of the add-on scripts we provide for adding software/functionality to the VM.
