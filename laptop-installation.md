---
layout: default
title: Laptop Installation
---
### Installing BCE on your laptop

1) Download and install Oracle VirtualBox from the [VirtualBox website](https://www.virtualbox.org/wiki/Downloads).

2) Download the BCE Virtual Machine (VM):

  - [BCE-2015-spring-preview-2.ova](https://berkeley.box.com/s/a4736ybkl7emdmnleu6f) (3.2GB; MD5: b6062814ebbef4d0e65cf2b42eac42d7)
  - [BCE-2015-spring.ova](https://berkeley.box.com/s/2g9x9c3q7qwhb9e4trwc) (3.4GB; MD5: 3d26353b7969ebcee6755529ae0751fc)

3) Open the VirtualBox application you installed in Step 1.

4) From the menu select **File > Import appliance** and locate the BCE .ova file you downloaded in step 2.

5) Wait a few minutes while the BCE .ova file is imported as a VirtualBox VM.

6) Once importing finishes, it will appear in the Powered Off state in the Oracle VM VirtualBox Manager. Select it, then click the **Start** button.

7) This will start a virtual Linux computer within your own machine.
  After a few seconds you should see black screen and then the VM's
  desktop.

### Installation trouble?

If you encountered problems during installation, here are some options:

- Attend the next scheduled group installation session where experts
  will help you install BCE, get you familiar with the environment, or
  help you find an alternative if your laptop is not capable of
  running BCE. The next session is: **11am-1pm, Jan 12th at D-Lab in 365 Barrows Hall.**

- Ask for help via email on the [BCE community support forum](https://groups.google.com/forum/#!forum/ucb-bce)

- Attempt to fix it yourself by trying our [Troubleshooting Tips](troubleshooting-tips.html).

### Using BCE

You now have a machine that has all the software installed as part of
BCE, including IPython, useful Python packages, R, RStudio, and useful
R packages.

You can get a terminal window that allows you to type commands in a
UNIX-style shell by clicking on the icon of the black box with the *$*
symbol on the top panel. You can start IPython Notebook in the
terminal by simply typing `ipython notebook`, or R by simply typing
`R`. This starts a bare-bones R session. To start RStudio, either type
`rstudio` at the prompt on go to **Applications > Programming >
RStudio**.

You can restart the VM at any time by opening VirtualBox and clicking
on the tab for the VM and clicking "Start" as you did above.
