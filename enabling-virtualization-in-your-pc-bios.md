---
layout: default
title: Enabling Virtualization in your PC BIOS
---
#### Enabling Virtualization in your PC BIOS

While most recent PCs support hardware virtualization, not all computer
vendors enable this feature as shipped from the factory. To turn this
feature on, try these instructions based on [Red Hat
instructions](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Virtualization_Administration_Guide/sect-Virtualization-Troubleshooting-Enabling_Intel_VT_and_AMD_V_virtualization_hardware_extensions_in_BIOS.html):

  * Reboot your computer
  * Right when the computer is coming up from the black screen, press
	**Delete**, **Esc**, **F1**, **F2**, or **F4**. Each computer manufacturer
	uses a different key but it may show a brief message at boot telling you
	which one to press. If you miss it the first time, reboot and try again. It
	helps to tap the key about twice a second when the computer is coming
	up. If you are not able to enter the BIOS via this method, consult your
	computer's manual.
  * In the BIOS settings, find the configuration items related to the CPU.
	These can be in under the headings **Processor**, **Chipset**, or
	**Northbridge**.
  * Enable virtualization; the setting may be called **VT-x**, **AMD-V**,
	**SVM**, or **Vanderpool**. Enable **Intel VT-d** or **AMD IOMMU** if the
	options are available.
  * Save your changes and reboot.

#### Check if your system supports Virtualization

If you are unable to find the Virtualization settings in your BIOS it
may mean that your laptop does not support it. If you want to try to
find this out yourself, then you can try:

  * On Windows,
    [download](http://www.microsoft.com/en-us/download/details.aspx?id=592) and
    run a Microsoft utility. You can also download utilities to [check if your CPU is capable of virtualization](http://www.technorms.com/8208/check-if-processor-supports-virtualization), if not enabled.
    [Hyper-V must be disabled](https://www.virtualbox.org/ticket/12350) in order for VirtualBox to run 64-bit guest operating systems. Visit the "turn Windows feature on or off" application and make sure Hyper-V is not checked.

  * On Linux, open a terminal window and run:

	```egrep -q 'vmx|svm' /proc/cpuinfo && echo yes || echo no```

#### What do I do if my laptop is not capable of Virtualization?

Don't worry! Come to the
[next BCE install session](http://ucberkeley.github.io/bce-documentation/help.html)
and an expert will help you determine if your hardware is capable and,
if not, can discuss alternatives to running on your laptop.

