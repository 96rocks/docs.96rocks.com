+++
title = "macOS"
description = "Install rkdeveloptool on macOS"
+++

To flash ROCK960 board, you need to install the rkdeveloptool, which is an open source cross platform command line tool. To build rkdeveloptool, you should have installed brew on your macOS.

Install build tools:

    brew install automake autoconf libusb

Clone the source code and build:

    git clone https://github.com/rockchip-linux/rkdeveloptool
    cd rkdeveloptool
    autoreconf -i
    ./configure
    make

Now you have rkdeveloptool executable at the current directory.
