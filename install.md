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

The current recommended release is 2015 Summer.

#### 

1) Download and install Oracle VirtualBox for:
  - Mac OS X
    - <span class="fa fa-apple fa-2x"></span> [2015 Summer](http://download.virtualbox.org/virtualbox/4.3.28/VirtualBox-4.3.28-100309-OSX.dmg) (108MB)
    - <span class="fa fa-apple fa-2x"></span> [2015 Fall](http://download.virtualbox.org/virtualbox/5.0.10/VirtualBox-5.0.10-104061-OSX.dmg) (86MB)
  - Windows
    - <span class="fa fa-windows fa-2x"></span> [2015 Summer](http://download.virtualbox.org/virtualbox/4.3.28/VirtualBox-4.3.28-100309-Win.exe) (105MB)
    - <span class="fa fa-windows fa-2x"<span></span> [2015 Fall](http://download.virtualbox.org/virtualbox/5.0.10/VirtualBox-5.0.10-104061-Win.exe) (112MB)
  - <span class="fa fa-linux fa-2x"></span> [Linux](https://www.virtualbox.org/wiki/Linux_Downloads)
  - Other versions available on [Oracle VirtualBox download page](https://www.virtualbox.org/wiki/Downloads).

2) Download the BCE Virtual Machine (VM) Appliance file (.ova):
  - [Summer 2015 (BCE-2015-summer.ova)](https://berkeley.box.com/s/68g11omap9yqow3a09t36wvwsuplio3w) (3.5GB)
    - (MD5 integrity checksum: 9e9500c00b7f2a1f0ac10623fbc6fbed)
  - [Fall 2015 (BCE-2015-fall.ova)](https://berkeley.box.com/s/wqnuag86gmdxd17za868gjdieym6phvp) (3.7GB)
    - (MD5 integrity checksum: db24805d6c40e93693f010494d3cd811)
  - Older versions of BCE are available from the [BCE Downloads page](downloads.html).
 
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

We provide both BCE-2015-fall and BCE-2015-spring versions for EC2. In general we recommend the newer BCE-2015-fall version, but for anyone wishing to use BCE with StarCluster, you should use BCE-2015-spring as BCE-2015-fall is incompatible with StarCluster.

#### Starting a BCE-based EC2 VM via the AWS console.

  - Go to the EC2 dashboard by logging onto AWS at the [AWS management console](https://console.aws.amazon.com/?nc2=h_m_mc), select **EC2**, and choose the us-west-2 (Oregon -- recommended due to cheaper pricing) or us-west-1 (N. California) region, as that is where we have posted the BCE AMI. (You’ll need to have an AWS account set up.)
  - On the **AMIs** tab, search for and select "BCE-2015-fall" amongst public images (the image IDs are ami-0c9a8d6d in us-west-2 and ami-78abc418 in us-west-1).
  - Launch an instance
  - Follow the instructions given in the **Connect** button to SSH to the instance. From the command line, this will look like `ssh -i ~/.ssh/your_ssh_key ubuntu@52.140.43.42` where the IP address after the '@' will be given in the instructions. 
  - After first logging in, we suggest you run our [*modify-for-aws.sh*](downloads.html) script to add some additional functionality specific to AWS. 
  - If you want to connect to the instance as the *oski* user, you can deposit your public SSH key in the .ssh folder of the *oski* user. The [*modify-for-aws.sh*](downloads.html) script will set this up so you can just ssh to `oski@<VM_IP_address>`. Alternatively you can do ````sudo su - oski```` from UNIX shell prompt after logging into the instance.

#### Starting a BCE-based EC2 virtual cluster via Starcluster

This will only work with BCE-2015-spring as StarCluster is not compatible with the newer version of Ubuntu used in BCE-2015-fall.

  - Install [Starcluster](http://star.mit.edu/cluster/docs/latest/installation.html). You could do this in your VirtualBox BCE VM if you like.
  - Modify our example Starcluster configuration file [starcluster_example.config](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/starcluster_example.config) to use your AWS credentials and account number and your SSH key pair. Save your config file in your home directory as *~/starcluster/.config*.
  - Follow the example code in [starcluster.sh](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/starcluster.sh) to start your virtual cluster and add parallel tools for Python and R. You'll need the various scripts for adding functionality to BCE from the [BCE Downloads page](downloads.html).
  - SSH to the cluster: `starcluster sshmaster -u oski mycluster`. Now you're ready to run your parallel computation.

Keep your eyes out here for future documentation for starting EC2 instances and clusters via Vagrant and boto.
