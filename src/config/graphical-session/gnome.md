# GNOME

## Pre-installation

Install the `dbus` package, ensure the `dbus` service is enabled, and reboot for
the changes to take effect.

## Installation

Install the `gnome` package for a GNOME environment which includes GNOME
applications.

A minimal GNOME environment can be created by installing the `gnome-session`,
`gdm` and `adwaita-icon-theme` packages. (Note, however, that not all GNOME
features may be present or functional.) `gdm` defaults to providing a Wayland
session, via the `mutter` window manager. For an Xorg session, install the
`xorg` package, then select 'GNOME on Xorg' at the GDM login screen, or start
`gnome-session` via `~/.xinitrc`.

If you require [ZeroConf](http://www.zeroconf.org/) support, install the `avahi`
package and enable the `avahi-daemon` service.

## Display Manager

To use a graphical display manager for logging in to GNOME, enable the `gdm`
service. Test the `gdm` service before enabling it:

```
# sv once gdm
```
