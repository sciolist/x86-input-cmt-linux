xf86-input-cmt on linux
=======================

Build and install the chrome os xf86-input-cmt driver.

There are a number of dependencies that you'll need to make sure you have available.
I haven't bothered to make a complete list, but here's a few for Ubuntu 18:

    apt get libjsoncpp-dev libglib2.0-dev libevdev-dev xutils-dev

To build and install, run:

    git submodule init
    ./build
    ./install

When installed, you'll need to add some X11 configuration.
The chromium configs are in src/xorg-conf, there's also a default configuration in "40-touchpad-cmt.conf"

To install the default configuration, run:

    sudo cp 40-touchpad-cmt.conf /usr/share/X11/conf.d/90-touchpad-cmt.conf

Restart X and with some luck you'll be good to go.
