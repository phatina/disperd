Disperd
=======

Disperd is an automatic switching daemon based on disper; it switches the
output on monitor hotplug.

Configuration
-------------

Behavior is based upon its configuration file stored at `~/.config/disperd.conf`.
Example of such file:

    [General]
    action = switch
    extend_direction = right

Possible actions performed when a hotplug event occurs:

  1. switch
  2. extend

Extension directions are taken from disper utility.


Disper
======

Disper is an on-the-fly display switch utility. It is intended to be used just
before giving a presentation with a laptop, when all one wants is that the
beamer, which has just been connected, is able to show whatever you prepared.

Disper gives you the option to either clone the all detected displays, or
extend the desktop to them. Resolutions are automatically detected. For
cloning, the highest resolution supported by all displays devices is chosen;
for extending every display device gets its highest supported resolution.
For special setups requiring more detailed control, one can still use the
standard display configuration utilites.

At the moment nVidia cards have the best support. XRandR is working, though
import/export is not complete. Contributions are welcome in this area.

Generally, one would bind 'disper -c' to a shortcut key (or if you rather
like to extend your desktop, use 'disper -e'). Without an external display
or beamer connected, you'll get your laptop's full resolution; when an external
display is present, it switches to clone mode after the keypress (or extend, if
you configured it that way).


Original Project
================

This project is based on:

http://willem.engen.nl/projects/disper/

- Willem van Engen <dev-disper@willem.engen.nl>

Many thanks.
