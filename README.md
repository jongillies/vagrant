# DevOps

## Prerequisites

* You must have Vagrant installed.

# Make your VM

To create the VM run the following command:

```bash
vagrant up
```

To SSH to the instances:

```bash
vagrant ssh
```

# Other Vagrant Commands

To destroy the VM:

```bash
vagrant destroy
```

# Nifty!

The working directory  from where you used Vagrant to "up" the machine is mounted to `/vagrant` in the virtual machine.  This is a nifty place where you can copy files back and forth between the host ane VM.
