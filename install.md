---
layout: default
title: Installation
---

BCE is currently available in two forms, both documented below.

  - Installing on your laptop.
  - Using BCE on Amazon EC2 instances.


### Installing BCE on your laptop or desktop computer

#### Do you have 14 Gb free space?

Before you begin, the download and install process **requires at least 14GB free** (only 10 Gb if you access the .ova file from a USB key or separate hard drive) on your hard drive or you are likely to encounter problems installing and running BCE due to out of disk space errors. If you do not have 14GB free, then visit the [help page](help.html) to inquire about other options.

1) Download and install Oracle VirtualBox for:

  - <span class="fa fa-apple fa-2x"<span></span> [Mac OS X VirtualBox-4.3.20-96996-OSX.dmg](http://download.virtualbox.org/virtualbox/4.3.20/VirtualBox-4.3.20-96996-OSX.dmg) (108MB)
  - <span class="fa fa-windows fa-2x"<span></span> [Windows VirtualBox-4.3.20-96997-Win.exe](http://download.virtualbox.org/virtualbox/4.3.20/VirtualBox-4.3.20-96997-Win.exe) (105MB)
  - <span class="fa fa-linux fa-2x"<span></span> [Linux](https://www.virtualbox.org/wiki/Linux_Downloads)
  - Other versions available on [Oracle VirtualBox download page](https://www.virtualbox.org/wiki/Downloads).

2) Download the latest BCE Virtual Machine (VM) Appliance file (.ova):

  - [Spring 2015 (BCE-2015-spring.ova)](https://berkeley.box.com/s/2g9x9c3q7qwhb9e4trwc) (3.4GB)
    - (MD5 integrity checksum: 3d26353b7969ebcee6755529ae0751fc)

3) Open the VirtualBox application you installed in Step 1.

4) From the menu select **File > Import appliance** and locate the BCE .ova file you downloaded in Step 2.

5) Wait a few minutes while the BCE .ova file is imported as a VirtualBox VM.

6) Once importing finishes, it will appear in the Powered Off state in the Oracle VM VirtualBox Manager. Select it, then click the **Start** button.

7) This will start a virtual Linux computer within your own machine.
  After a few seconds you should see black screen and then the VM's
  desktop.

**Installation trouble?** See our [help page](help.html).

We provide [screencasts](screencasts.html) demonstrating installation based on these instructions.

### Running BCE on EC2 instances

NEWS: The BCE-spring-2015 image (AMI) for Amazon's EC2 is now available.

  - Go to the EC2 dashboard by logging onto AWS at the [AWS management console](https://console.aws.amazon.com/?nc2=h_m_mc), select **EC2**, and choose the us-west-1 (N. California) or us-west-2 (Oregon) region, as that is where we have posted the BCE AMI. (You’ll need to have an AWS account set up.)
  - On the **AMIs** tab, search for and select "BCE-spring-2015" amongst public images (the image IDs are ami-958e6bd1 in us-west-1, and ami-cdf5d3fd in us-west-2).
  - Launch an instance
  - Follow the instructions given in the **Connect** button to SSH to the instance. From the command line, this will look `ssh -i ~/.ssh/your_ssh_key ubuntu@52.140.43.42` where the IP address after the '@' will be given in the instructions. 
  - After first logging in, we suggest you run our [*modify-for-aws.sh*](downloads.html) script to add some additional functionality specific to AWS. 
  - If you want to connect to the instance as the *oski* user, you can deposit your public SSH key in the .ssh folder of the *oski* user. The [*modify-for-aws.sh*](downloads.html) script will set this up so you can just ssh to `oski@<VM_IP_address>`. Alternatively you can do ````sudo su - oski```` from UNIX shell prompt after logging into the instance.

Soon we hope to post tips on creating an EC2 virtual cluster with multiple connected nodes, either using StarCluster or the Python boto package.

### Download older versions of BCE

Older versions of BCE are available from the [BCE Downloads page](downloads.html).
