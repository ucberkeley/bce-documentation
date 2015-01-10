---
layout: default
title: Laptop Installation
---
### Getting the VM up and running

  * Download and install VirtualBox from the [VirtualBox
    website](https://www.virtualbox.org/wiki/Downloads).
  * Download the BCE Virtual Machine (VM): [3.2GB file named BCE-2015-spring-preview-2.ova](https://docs.google.com/uc?id=0Bz_1EI3c_TA1VzlScXUxaEEwSm8&export=download)
  * Open VirtualBox, go to File > Import appliance, and then select the .ova file you just downloaded (possibly located in the "Downloads" folder in your home directory).
  * Wait a few minutes while the OVA file is imported as a VirtualBox Virtual Machine (VM)
  * Start the virtual machine by clicking on the tab for
	"BCE-2015-spring-preview-2" on the left side and then clicking
	"Start" at the top. This will start a virtual Linux computer
	within your own machine.  After a few seconds you should see black
	screen and then the VM's desktop.

### Using BCE

You now have a machine that has all the software installed as part of BCE,
including IPython, useful Python packages, R, RStudio, and useful R packages.

You can get a terminal window that allows you to type commands in a
UNIX-style shell by clicking on the icon of the black box with the *$*
symbol on the top panel. You can start IPython Notebook in the terminal by
simply typing `ipython notebook`, or R by simply typing `R`. This starts a
bare-bones R session. To start RStudio, either type `rstudio` at the prompt
on go to **Applications > Programming > RStudio**.

You can restart the VM at any time by opening VirtualBox and clicking on the tab
for the VM and clicking "Start" as you did above.
