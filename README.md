# dwm - dynamic window manager

dwm is an extremely fast, small, and dynamic window manager for X.

See [this link](https://dwm.suckless.org) for the original source/creators of dwm.

## Requirements

-Xlib header files are required to build dwm.

## Installation

Edit config.mk to match your local setup (dwm is installed into the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if necessary as root):

```sh
$ make clean install
```

## Running dwm

Add the following line to the end of your `.xinitrc` to start dwm using startx:

```sh
exec dwm
```

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

```
DISPLAY=foo.bar:1 exec dwm
```

(This will start dwm on display :1 of the host foo.bar)

## Status bar

The status bar is set with `xsetroot -name "$status"`.

An example script exists in the `scripts` directory.

It is recommended to add these to your `PATH` - for example, I've created `$HOME/.local/bin` and added it to my path in `$HOME/.xprofile`. Then, in `$HOME/.xinitrc`, I have the line `dwmbar &` before `exec dwm`.
