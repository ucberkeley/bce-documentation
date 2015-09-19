---
layout: default
title: Downloads
---

## Current BCE Virtual Machine (VM)

  - [Summer 2015 (BCE-2015-summer.ova)](https://berkeley.box.com/s/68g11omap9yqow3a09t36wvwsuplio3w) (3.5GB)
    - (MD5 integrity checksum: 9e9500c00b7f2a1f0ac10623fbc6fbed)

  - Scripts to add functionality to BCE ([instructions for how to run these scripts](patch.html))
    - [Adding functionality for AWS (modify-for-aws.sh)](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/modify-for-aws.sh)
    - [Add tools for parallel computing (add-parallel-tools.sh)](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/add-parallel-tools.sh) NOTE: Python tools install successfully only in BCE-spring-2015 (see below).
    - [Add tools for parallel computing to Starcluster worker nodes (add-parallel-starcluster.sh)](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/add-parallel-starcluster.sh) NOTE: use only with BCE-spring-2015 (see below); Starcluster and BCE-summer-2015 conflict.

## Release schedule

We plan to release a new version of BCE at the start of each semester (January for spring semester, May for summer, and August for fall). We will also prepare preview versions a couple of weeks prior to these official releases that will allow us to test and get feedback.

As need arises, we will release patches to fix issues in the official release. These patches will simply be code files that a user can run within the VM to update the VM.

## Older releases

  - [Spring 2015 (BCE-2015-spring.ova)](https://berkeley.box.com/s/2g9x9c3q7qwhb9e4trwc) (3.4GB)
    - (MD5 integrity checksum: 3d26353b7969ebcee6755529ae0751fc)
    - Patch file: none ([patching instructions](patch.html))

## Upcoming preview versions

  - To appear in summer 2015: Fall 2015 preview

### Older preview versions

  - [Spring 2015 Preview #2 (BCE-2015-spring-preview-2.ova)](https://berkeley.box.com/s/a4736ybkl7emdmnleu6f) 
    - (3.2GB; MD5: b6062814ebbef4d0e65cf2b42eac42d7)
