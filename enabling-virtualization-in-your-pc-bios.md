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
