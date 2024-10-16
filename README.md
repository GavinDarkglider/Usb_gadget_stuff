I release this under gplv2.

Information:

This is my attempt at figuring out the usb gadget subsystem in the linux kernel. i based this off of the bash bunny.

Currently the script is configured to work on the Nintendo Switch. To change that flip the commented line here, and comment out the uncommented line.
https://github.com/GavinDarkglider/Usb_gadget_stuff/blob/main/ATTACKMODE#L77-L78

Background services starting uses openrc,not systemd as i prototyped this on gentoo 
I also didn't include dhcpd config.

I take no responsibility for how people choose to use this information.

The patch file is my horrible attempt to add bashbunny metric spoofing like the bash bunny.
Unlike most options for this, you can set metric in userspace, like bash bunny, where most clones patch higher in kernel module and it isnt configurable.

This patch specifically is for l4t 4.9 kernel, but the code is easily ported to newer, mostly line differences, not code.
On the nintendo switch, if you want a gadet that sets itself up automatically on connection to PC, see this:
https://github.com/libretro/Lakka-LibreELEC/blob/Lakka-v5.x/projects/L4T/devices/Switch/packages/usb-gadget-scripts/udev.d/92-usb-gadgets.rules

I should also mention, i did not add the bash bunny background framework. All this is is my recreation of the gadget setup script they used, made to work as it did on the device. I did document other devices than they used as well, even if they arent used by the bash bunny.
