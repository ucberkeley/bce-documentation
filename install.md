---
layout: default
title: Laptop Installation
---

BCE is currently available in two forms, both documented below.

  - Installing on your laptop.
  - Using BCE on Amazon EC2 instances.

### Installing BCE on your laptop or desktop computer

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

### Running BCE on EC2 instances

[UNDER CONSTRUCTION - we don't currently have the BCE Spring 2015 VM available for EC2 but hope to do shortly. In the meantime you can test things out using one of our older beta version (BCE-0.1.7) AMIs as described here.]

  - Go to the EC2 dashboard by logging onto AWS at the [AWS management console](https://console.aws.amazon.com/?nc2=h_m_mc), select **EC2**, and choose the us-west-1 (N. California) or us-west-2 (Oregon) region, as that is where we have posted the BCE AMI. (You’ll need to have an AWS account set up.)
  - On the **AMIs** tab, search for and select the most recent BCE AMI amongst public images (currently ami-2d9a8b68 in us-west-1, and ami-1feabf2f in us-west-2).
  - Launch an instance
  - Follow the instructions given in the **Connect** button to SSH to the instance
  - If you want to connect to the instance as the *oski* user, you can deposit your public SSH key in the .ssh folder of the *oski* user. Alternatively you can do ````sudo su - oski```` from UNIX shell prompt after logging into the instance.

Eventually we hope to post tips on creating an EC2 virtual cluster with multiple connected nodes, either using StarCluster or the Python boto package.

### Download older versions of BCE

Older versions of BCE are available from the [BCE Downloads page](/downloads.html).
