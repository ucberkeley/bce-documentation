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
symbol on the top panel. You can start:

  - IPython Notebook by typing `ipython notebook` in the terminal or clicking on **Applications > Programming > IPython Notebook**.
  - A bare-bones R session by typing `R` in the terminal or clicking on **Applications > Programming > R**.
  - RStudio by typing `rstudio` in the terminal or clicking on **Applications > Programming > RStudio**.

#### Stopping and restarting the VM on your laptop

To stop the VM, simply click the red power button in the upper right.

You can restart the VM at any time by opening VirtualBox and clicking
on the tab for the VM and clicking "Start" as you did above.

#### Using shared folders to move files between the VM and your laptop

One useful thing will be to share folders between the VM and the host machine so that you can access the files on your computer from the VM. Do the following:

  - On the VirtualBox Taskbar go to **Devices > Shared Folder Settings** and click on the icon of a folder with a “+” on the right side.
  - Select a folder to share, e.g. your home directory on your computer by clicking on the down arrow by **Folder Path** and choosing **Other** and navigating to the folder of interest. For our purposes here, assume we click on “Documents”.
  - Click **Auto-mount** and **Make permanent** and then click **Ok** twice.
  - Reboot the machine by clicking on the red power button on the upper right and choosing **Restart**.
  - Once the VM is running again, click on the **Shared** folder on the desktop. You should see the folder **sf_Documents** (or whatever the folder name you selected was, in place of “Documents”). You can drag and drop files into and out of the folder.
  - Alternatively, from the Terminal, you can also see the directory by doing `cd ~/Desktop/Shared/sf_Documents` and then `ls` will show you the files. 
  - Be careful. Unless you selected **Read only** at the same time as **Make permanent**, any changes to the shared folder on the VM affects the folder in the *real world*, namely your computer.

#### Changing the memory (RAM) and number of CPUs of your VM

Before starting the VM, click on the **Settings** icon in the VirtualBox Manager window task bar. Select **System**. To increase memory, click on **Motherboard** and adjust the **Base Memory** slider.  To increase the number of virtual CPUs to be more than the default of one, click on **Processor** and adjust the **Processor(s)** slider. In general you would not want to select more processors than the host machine has cores.

At the moment, you cannot increase the amount of disk space associated with the VM beyond 16 Gb, but you can of course use Shared Folders to access the disk on the host machine.
