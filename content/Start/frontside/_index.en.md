---
title: Front Side
weight: 12
---

## Front side of the board

The main components on the front side of rock960 are labeled as below:

![Front side with label](/Start/frontside/images/rock960_top_with_label.png)

* **Low Speed Connector**: 96boards CE standard low speed expansion connector. Pin definition can be found at [96boards pinout](https://www.96boards.org/pinout/)
* **Debug UART**: Low level debug message output, the default baud rate for rock960 is 1500000. You need [USB to TTL]() to connect to host PC. Configure serial tool on host PC.
* **Reset Key**: Hardware reset key
* **Maskrom Key**: Maskrom key is for upgrading the firmware on EMMC or boot from USB. Check Rockchip wiki about [Maskrom mode](http://opensource.rock-chips.com/wiki_Rockusb#Maskrom_mode)
* **High Speed Connector**: 96boards CE standard high speed expansion connector, with two MIPI channel and I2C
* **BT/WIFI Chip**: AP6356s, 802.11 ac/a/b/g/n, 2xMIMO
* **BT/WIFI Antenna**: On board antenna for BT/WIFI.
