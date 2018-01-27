---
title: Fastboot
weight: 50
---

## Introduction

Fastboot is a USB protocol for the host to communicate with the target android device at bootloader stage. Rockchip implements the fastboot protocol in u-boot, so ROCK960 use fastboot functionality.

## How to go to fastboot mode
There are 2 ways to go to fastboot mode

- In u-boot serial console, type `fastboot` command to go to fastboot mode
- In android shell, run `adb reboot fastboot` or `reboot fastboot` to reboot to fastboot mode. **Note:** `adb reboot bootloader` or `adb reboot loader` will reboot to [Rockusb mode](http://opensource.rock-chips.com/wiki_Rockusb), not fastboot mode.

## Supported fastboot commands 

### Get info command

    fastboot getvar version                             #get the version
    fastboot getvar version-bootloader                  #get the bootloader version
	fastboot getvar unlocked                            #check if unlocked
    fastboot getvar secure                              #check if locked
    fastboot getvar product                             #get product name
    fastboot getvar serialno                            #get serial number
    fastboot getvar partition-type:<partition_name>     #get partition type
    fastboot getvar partition-size:<partition_name>     #get partition size
    fastboot getvar partition-offset:<partition_name>   #get partition offset

### Lock/Unlock command

	fastboot oem unlock
	fastboot oem unlock_accept
	(oem unlock_accept command must be input within 5 seconds after oem unlock command)

	fastboot lock                 #lock the devices

### Write images command
You must unlock the device first and then write images.

	fastboot flash <partition_name> <file_name>
	(For example, fastboot flash system system.img)
	(Note: the partition name for parameter/loader is "parameter"/"loader")

### Reboot command

	fastboot oem recovery               #reboot to recovery
	fastboot oem recovery:wipe_data     #reboot to factory reset
	fastboot reboot                     #just reboot
	fastboot reboot-bootloader          #reboot to rockusb mode
	fastboot continue                   #normal boot
