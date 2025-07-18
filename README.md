-=(SparcStation_Senhor notes)=-

Tested: Working Video 720p, 1080p.

___
# SparcStation 

Author: [Grabulosaure](https://github.com/Grabulosaure)

There are two versions
- SparcStation5 : Single CPU. MicroSparcII compatible CPU. Up to around 65MHz. SS5 is compatible with all the OSes which supported actual Sun4m SparcStations : Linux, NetBSD, OpenBSD, SunOS, Solaris, NextSTEP. Some OSes requires a special configuration.
- SparcStation20 : Up to 3 CPUs can fit in MiSTer FPGA. SMP with write-back caches, MESI coherency. SuperSparc compatible CPU. Up to around 50MHz. SS20 seems to work with NetBSD with 3 CPUs. This is quite complex code and difficult to validate. Linux hardy ever supported multicore on these computers. I would like to be able to run multicore Solaris. IIRC, the debug monitor (/soft/debugarm) is currently needed to properly activate SMP mode.

Use OS images in http://temlib.org/pub/mister/SS/ , passwords are the OS names, uppercase and lowercase characters (NeXTSTEP, Solaris, SunOS). You can also make your own images using QEMU, or a real SparcStation.

The Ethernet interface isn't enabled on MiSTer. It used to work on the Xilinx board with a direct MII PHY.

Currently it has no sound support.

Source: https://misterfpga.org/viewtopic.php?t=4421
___
The core requires boot.rom to be copied in games/SparcStation

When you load the core you will have to wait about 1 minute and 20 seconds
for the video to appear. The core works like that and it's not a bug.

Instructions to boot NeXT STEP:

Load the SparcStation5 core and then in the OSD menu do the following:
- "Mount *.RAW" : Select next.raw file
- Select IOMMU rev: 11

Wait for 2'30"

Type "-v" in boot menu

Type Ctrl-C when waiting for network configuration server.




