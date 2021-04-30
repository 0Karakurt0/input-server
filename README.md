First of all, this is only a template for now, an evened-up ground to put all ideas into one place.

### So, what do I want from input server? 

I want to make one and only interface for interacting with inputs, not Xorg depended, nor any Wayland compositor.
It's quickly becomes an annoying mess when you try implementing something out of the ordinary.
It should also manage inputs for tty-s and from any non-standard inputs, like tablets or gamepads.

### Features
 - xdg compatable interface (so that minimal patching is requered. And I'm too laixy to try inventing a new standard)
 - Wayland-oriented (mainly because I'm beting on Wayland's succes)
 - sequrity mode - only send characters and modyfiers, with no connection to real keycodes on scancodes
 - make virtual inputs equal, so that, for example, keyboard of ssh client was seen the same way as physically connected one
 - pass-through mode - there's a lot of applications that depend on reading keys directly, so this mode should provide some compatability
 - layut support - no more strange ways to determine layout, this one deamor reads inputs so it is also the one how to interpret them (depends on sending only characters...)
 - keybindings support?
 - mapping and remapping config file
 - auto-detecting keys
