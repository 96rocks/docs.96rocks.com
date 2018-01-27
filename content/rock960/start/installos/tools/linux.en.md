+++
title = "Linux"
description = "Install rkdeveloptool on Linux"
+++

To flash ROCK960 board, you need to install the rkdeveloptool, which is an open source cross platform command line tool. To build rkdeveloptool, follow the instructions below:

Install build tools:

    sudo apt-get install libudev-dev libusb-1.0-0-dev dh-autoreconf

Clone the source code and build:

    git clone https://github.com/rockchip-linux/rkdeveloptool
    cd rkdeveloptool
    autoreconf -i
    ./configure
    make

Now you have rkdeveloptool executable at the current directory.
