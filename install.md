---
layout: default
title: Installation
---

BCE is currently available in two forms, both documented below.

  - Installing on your laptop.
  - Using BCE on Amazon EC2 instances (including use with CfnCluster).


### Installing BCE on your laptop or desktop computer

#### Do you have 14 Gb free space?

Before you begin, the download and install process **requires at least 14GB free** (only 10 Gb if you access the .ova file from a USB key or separate hard drive) on your hard drive or you are likely to encounter problems installing and running BCE due to out of disk space errors. If you do not have 14GB free, then visit the [help page](help.html) to inquire about other options.

The current recommended release is 2015 Fall.

1) Download and install Oracle VirtualBox for:

  - Mac OS X

    - <span class="fa fa-apple fa-2x"></span> [2015 Fall](http://download.virtualbox.org/virtualbox/5.0.10/VirtualBox-5.0.10-104061-OSX.dmg) (86MB)
    - <span class="fa fa-apple fa-2x"></span> [2015 Summer](http://download.virtualbox.org/virtualbox/4.3.28/VirtualBox-4.3.28-100309-OSX.dmg) (108MB)
  - Windows

    - <span class="fa fa-windows fa-2x"></span> [2015 Fall](http://download.virtualbox.org/virtualbox/5.0.10/VirtualBox-5.0.10-104061-Win.exe) (112MB)
    - <span class="fa fa-windows fa-2x"></span> [2015 Summer](http://download.virtualbox.org/virtualbox/4.3.28/VirtualBox-4.3.28-100309-Win.exe) (105MB)
  - <span class="fa fa-linux fa-2x"></span> [Linux](https://www.virtualbox.org/wiki/Linux_Downloads)
  - Other versions available on [Oracle VirtualBox download page](https://www.virtualbox.org/wiki/Downloads).

2) Download the BCE Virtual Machine (VM) Appliance file (.ova):

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

#### Starting a BCE-based EC2 virtual cluster via CfnCluster

CfnCluster allows you to easily start up multiple EC2 instances to form your own Linux cluster. You can then login to the master node of the cluster and submit jobs via a scheduler that will manage those jobs. One of the nice things about CfnCluster is that if you request more cores or nodes than are available, additional EC2 instances will be added to your cluster dynamically. And unused instances will be terminated to save you money. 

  - Install [CfnCluster](http://cfncluster.readthedocs.io/en/latest/getting_started.html). You should install version 1.3.1 as that is compatible with the BCE image for CfnCluster. CfnCluster provides a command line interface (CLI) written in Python, and is installable via `pip` and `easy_install`. You could do this in your VirtualBox BCE VM if you like.
  - Modify our example CfnCluster configuration file [cfncluster_example.config](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/cfncluster_example.config) to use your AWS credentials and account number and your SSH key pair, as well as a VPC ID and subnet ID available for your AWS account. Save your config file in your home directory as *~/.cfncluster/config*. 
  - Invoke `cfncluster create mycluster` to start your virtual cluster. Note that the AMI is only available in the us-west-2 region.
  - SSH to the cluster using the `MasterPublicIP` printed to the screen at the end of the CfnCluster startup process and with the flag `-i ~/.ssh/ec2.pem` where you should use the name of your private key in place of `ec2.pem`. Now you're ready to run your parallel computation.
  - You may need to start SLURM: if running `squeue` gives an error, then run `sudo /etc/init.d/slurm start`.
  - You can now start jobs from the master node of your cluster using syntax such as `srun --nodes=2 --ntasks=4 --pty /bin/bash` (for an interactive job) or `sbatch --nodes=2 --ntasks=4 myjob.sh` for a batch job.

#### Using BCE with an GPU-based EC2 instance

We've created a version of BCE with software for GPU computation, in particular CUDA, PyCUDA, RCUDA, and MAGMA. Simply choose the "BCE-2015-fall-gpu" public image (ami-5154b331) in the us-west-2 (Oregon) region.

#### Starting a BCE-based EC2 virtual cluster via Starcluster 

This use case is deprecated; we recommend use of BCE with CfnCluster (see above).

This will only work with BCE-2015-spring as StarCluster is not compatible with the newer version of Ubuntu used in BCE-2015-fall.

  - Install [Starcluster](http://star.mit.edu/cluster/docs/latest/installation.html). You could do this in your VirtualBox BCE VM if you like.
  - Modify our example Starcluster configuration file [starcluster_example.config](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/starcluster_example.config) to use your AWS credentials and account number and your SSH key pair. Save your config file in your home directory as *~/.starcluster/config*.
  - Follow the example code in [starcluster.sh](https://raw.githubusercontent.com/ucberkeley/bce/dev/post-install/starcluster.sh) to start your virtual cluster and add parallel tools for Python and R. You'll need the various scripts for adding functionality to BCE from the [BCE Downloads page](downloads.html).
  - SSH to the cluster: `starcluster sshmaster -u ubuntu mycluster`. Now you're ready to run your parallel computation.

Keep your eyes out here for future documentation for starting EC2 instances and clusters via Vagrant and boto.
