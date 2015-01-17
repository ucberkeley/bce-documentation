---
layout: default
title: Troubleshooting Tips
---
### Troubleshooting Tips

The most common problems across all types of laptops are:

* Not enough free space on your hard drive
* Not enough RAM system memory

There is tremendous variation between hardware across laptop
manufacturers, and below we list the most common known problems and
their solutions.

#### Apple Laptops

Most Apple laptops released in the last few years are capable of
running BCE, however some older Apple laptops do not support the
hardware virtualization required to run a Virtual machine.

#### PC Laptops

##### Is your Virtualization feature turned on?

While many recent PC laptops support hardware virtualization, some
computer vendors disable this feature as shipped from the factory.

If you are familiar with changing settings in your system BIOS, you
may try: [Enabling Virtualization in your PC BIOS](enabling-virtualization-in-your-pc-bios.html).

However, many older, and even some brand new, PC laptops do not
support hardware virtualization at all.

#### Other possible issues

  - Check that you have the complete .ova file downloaded by comparing the file size on your computer to the information on our [downloads page](/bce-documentation/downloads.html).
  - If you get a text-based screen with some wording about a UEFI shell, try clicking on the **Settings** tab for the **Oracle VM VirtualBox Manager** window and clicking on **System**. Under the **Motherboard** page, be sure that **Enable EFI (special OSes only)** is unchecked. Then click **OK**, and try to start the VM again. 
