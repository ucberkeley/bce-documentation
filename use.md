---
layout: default
title: Using BCE
---

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

#### Stopping and restarting the VM on your laptop

To stop the VM, simply click the red power button in the upper right.

You can restart the VM at any time by opening VirtualBox and clicking
on the tab for the VM and clicking "Start" as you did above.

#### Using shared folders to move files between the VM and your laptop

One useful thing will be to share folders between the VM and the host machine so that you can access the files on your computer from the VM. Do the following:

  - Go to “Devices > Shared Folder Settings” and click on the icon of a folder with a “+” on the right side.
  - Select a folder to share, e.g. your home directory on your computer by clicking on “Folder Path” and choosing “Other” and navigating to the folder of interest. For our purposes here, assume we click on “Documents”.
  - Click “make permanent” and “auto-mount” and then click “Ok”.
  - Reboot the machine by going to applications button on the left of the top toolbart, clicking on “Log Out”, and choosing “Restart” in the window that pops up.
  - Once the VM is running again, click on the “Shared” folder on the desktop. You should see the folder “sf_Documents” (or whatever the folder name you selected was, in place of “Documents”). You can drag and drop files to manipulate them.
  - Alternatively, from the Terminal, you can also see the directory by doing “cd ~/Desktop/shared/sf_Documents” and then “ls” will show you the files. Be careful: unless you selected “read only” at the same time as “make permanent”, any changes to the shared folder on the VM affects the folder in the real world, namely your computer.
