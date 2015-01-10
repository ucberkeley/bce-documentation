---
layout: default
title: BCE
---
### What is BCE?

BCE stands for the Berkeley Common (or Compute, or Collaborative...) Environment.
It is designed to provide a common Linux computational environment for classwork
and research.

### BCE Vision

The goal for the BCE is to provide both the ready-made environments and also
the "recipes" or scripts setting up these environments. It should be easy for a
competent Linux user to create recipes for custom tools that might not be
broadly useful (and thus, not already in BCE).

BCE is designed for classwork and research in the sciences at Berkeley, broadly defined to
include social science, life science, physical science, and engineering. Using
these tools, users can start up a virtual machine (VM) with a standardized Linux
operating environment containing a set of standard software for scientific
computing. The user can start the VM on their laptop, on a university server, or
in the cloud. Furthermore, users will be able to modify the instructions for
producing or modifying the virtual machine in a reproducible way for
communication with and distribution to others.

We envision the following core use cases:

  - creating a common computing environment for a course or workshop,
  - creating a common computational environment to be shared by a group of researchers or students, and
  - disseminating the computational environment so outsiders can reproduce the results of a group.

What problems does BCE solve for you?

 - No more obscure installation issues - download and run a single virtual
   machine or get the same environment on a bare metal or virtual server.
 - I'm teaching a class - when you tell a student that a program behaves a
   certain way, it does!
 - I'm collaborating on some scientific research - now all of your collaborators
   can run your code without complex installation instructions.

To accomplish this, we envision that BCE will encompass the following:

 - a reproducible workflow that creates the standard VM/image
   with standard scientific computing software such as Python, R, git, etc.,
 - a standard binary image, produced by the workflow, that can be distributed as is and
   used on-the-fly with VirtualBox or VMWare Player with minimal dependencies, and
 - (possibly) an augmented workflow that represents multiple possible distributions tailored
   for different types of uses (e.g., different disciplines, different
   computational needs, class vs. research use, etc.). This might
   represent either a sequence or a tree of possible VMs.

### Who are we?

BCE is a project started by
[D-Lab](http://dlab.berkeley.edu)
and the
[SCF (Statistical Computing Facility)](http://statistics.berkeley.edu/computing).
Current collaborators include
[BRC (Berkeley Research Computing)](http://research-it.berkeley.edu/brc),
[the School of Information](http://ischool.berkeley.edu),
[the Linguistics Department](http://linguistics.berkeley.edu/plab/guestwiki/index.php?title=Berkeley_Phonetics_Machine),
and other independent contributors.
