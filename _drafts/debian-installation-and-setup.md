---
layout: "post"
title: "Debian installation and configuration"
date: "2017-03-20 15:41"
comments: true
---

## OS Install
I decided to go with Debian for the operating system because I wanted to be able to use the [NeuroDebian](http://neuro.debian.net/) repository. I may experiment with other Debian derivatives in the future. I wrote the Live disk image for Debian 8 "Jessie" (with firmware + nonfree) to a bootable USB drive for the installation.

After installation, at first I was stuck in tty1---could not get the X window system to start. Adding the following Grub options at the end of the ```linux``` call allowed me to start the GNOME desktop with the nouveau graphics driver:
```nomodeset xforcevesa vga=791```.

## NVIDIA Driver


Useful packages/commands for debugging:
* ```nvidia-detect```
* ```xstart``` or ```xinit```
* ```modinfo```
* ```dkms status```
* ```inxi -Fxz```
* ```lsmod | grep nvidia```
* ```lshw -s video```
* ```lspci | grep VGA```

## CUDA Toolkit


## VPN
* to replace Cisco AnyConnect VPN: ```sudo apt-get install openconnect```
* NetworkConnect requires 32-bit libraries

## Disk partitionning

## Benchmarking

## Dotfiles and configurations

## Development environment
Conda
