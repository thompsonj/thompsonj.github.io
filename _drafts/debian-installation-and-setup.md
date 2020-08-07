---
layout: "post"
title: "Debian installation and configuration"
date: "2017-03-20 15:41"
comments: true
---

## OS Install
I decided to go with Debian for the operating system because I wanted to be able to use the [NeuroDebian](http://neuro.debian.net/) repository. I may experiment with other Debian derivatives in the future. I wrote the Live disk image for Debian 8 "Jessie" (with firmware + nonfree) to a bootable USB drive for the installation.

After installation, at first I was stuck in tty1---could not get the X window system to start. Adding the following Grub options at the end of the ```linux``` call allowed me to start the GNOME desktop with the nouveau graphics driver: ```nomodeset xforcevesa vga=791```

## NVIDIA Driver
Conflicting instructions from [Debian](https://wiki.debian.org/NvidiaGraphicsDrivers#jessie-375) and during the installation itself.

IIRC the important steps for getting it to work was:
* making sure nouveau is properly blacklisted
* xorg config to use nvidia driver
* Make sure X module path reaches nvidia X driver (found in /usr/lib/nvidia/nvidia). X was looking only in /usr/lib/xorg/modules/drivers.

Useful packages/commands for debugging:
* ```nvidia-detect```
* ```xstart``` or ```xinit```
* ```modinfo```
* ```dkms status```
* ```inxi -Fxz```
* ```lsmod | grep nvidia```
* ```lshw -s video```
* ```lspci | grep -i nvidia```


## CUDA Toolkit
* Need CUDA 8 for Pascal GPU architecture and Tensorflow v1
* CUDA 8 not officially supported on Debian
* Want to use Debian for Neurodebian (and don't want to use Ubuntu)

<!-- Originally installed CUDA toolkit using Ubuntu 16.04 runfile,
but later realized it lists gcc 5 as minimum requirement, which is only available in debian testing. However, I did manage to install that version and was able to compile CUDA examples successfully. However, they won't run and give me the error "Failed to allocate device vector A (error code CUDA driver version is insufficient for CUDA runtime version!)" Despite that I have NVIDIA 375.26 installed which seems to be the same version that comes with the CUDA toolkit.

assuming similar to Ubuntu 14.04 install so follow those instructions -->
<!--
Requirement  | Version  | Installed
--|---|--
Kernel  | 3.13	  |  3.16
GCC	    | 4.8.2	  |  4.9.2
GLIBC	  |  2.19   |  2.19 (libc-bin and associated packages)
ICC     | 	16.0  |
PGI		  |  16.3+  |
XLC		  | NO      |
CLANG   | 3.8+    |  3.8 (use update-alternatives to specify 3.8 over 3.5) -->

Originally I installed the CUDA 8 toolkit using the Ubuntu 16.04 runfile and skipped the NVIDA driver install since I already had the correct driver installed (375.26). However, I kept getting errors like, "Failed to allocate device vector A (error code CUDA driver version is insufficient for CUDA runtime version!)". In the end, I had to uninstall the NVIDIA driver and use the CUDA runfile to install both the NVIDIA driver and the CUDA 8 toolkit at the same time.

1. uninstall existing NVIDIA driver ```sudo apt-get purge nvidia* u```
2. uninstall CUDA ```/usr/local/cuda-8.0/bin/uninstall```
3. reboot ```sudo systemctl reboot```
4. Login to text only shell, quit any xwindow server that begins
5. Run CUDA runfile to install both NVIDIA graphics driver and CUDA 8 toolkit
./cuda installation .run

## Tensorflow
* Install Tensorflow v1.0
  * install from sources in order to enable advanced instruction sets
    * requires bazel
      * requires java 7 or 8
      * add custom apt repository https://bazel.build/versions/master/docs/install-ubuntu.html
  * cudnn v5.1 (v6 just came out!)

## VPN
* openconnect to replace Cisco AnyConnect VPN: ```sudo apt-get install openconnect```
* NetworkConnect requires 32-bit libraries - annoying!

## Disk partitionning
At initial assembly, I installed two SSDs: one 260GB drive for the OS and one 1TB m.2 NVME drive for fast access to data.
#### Samsung 850 EVO 250GB 2.5" Solid State Drive
Three partitions:
1. current: 84GB, boots to Debian
2. next: 84GB, for when I want to upgrade to a new OS, I can install here without touching my current OS.
3. swap: 64GB, same size as the RAM so that it can be used for hibernation

#### Samsung 960 EVO 1TB m.2-2280 Solid State Drive
One partition.

A few months after assembly, I upgrade the storage by adding:
#### Samsung 960 EVO 1TB m.2-2280 Solid State Drive
The ASRock Taichi X99 motherboard has 2 m.2 ports so I decided to add another Samsung 960 EVO 1TB which allowed me to configure the two drives in RAID 0 giving me lightning fast read and write speeds for 2TB of storage.

#### Crucial 2TB 2.5" Solid State Drive
The Phanteks Enthoo Pro ATX full tower case comes with one SSD bracket tucked away on the back of the case behind the motherboard, but there is actually a mount for a second SSD bracket slightly lower on the back plate. So I ordered another bracket and installed this 2nd 2.5" SSD without using any of the disk bays (which I removed during assembly to increase airflow). At this point, I have 250GB + 1TB + 1TB + 2TB = 4250GB of storage in this tower without using any of the disk bays.

#### Wester Digital 8TB My Book external hard drive
Although the RAID 0 array increases access speed, it also increases the risk of data loss. This external is large enough to keep everything safely backed up at all times.

## Benchmarking
Here you can see that the 2TB RAID 0 array acheives average read speeds of 5.9 GB/s and write speeds of 2.5 GB/s.

<!-- ## Dotfiles and configurations -->

<!-- ## Development environment
* Conda
* NeuroDebian repository
  * fslview
  * python-nipype
  * python-mvpa2
* Atom
  * link to gist
  * tricky getting Hydrogen to inherit conda environment, had to install ipykernel and run python -m ipykernel install --user --name tf --display-name "Python (tf)" after which I had to reinstall the tensorflow whl for some reason
  * -->

<!-- ## Programs
* MATLAB
* BrainVoyager

## MATLAB toolboxes
* NeuroElf -->
