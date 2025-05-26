
Important:
When you load the core you will have to wait about 1 minute and 20 seconds
for the video to appear. The core works like that and it's not a bug.


There are two compilation modes
- SS5 : SparcStation 5 : Single CPU. MicroSparcII compatible CPU. Up to around 65MHz.
- SS20 : SparcStation 20 : Up to 3 CPUs can fit in MiSTer FPGA. SMP with write-back caches, MESI coherency. SuperSparc compatible CPU. Up to around 50MHz.
  
SS5 is compatible with all the OSes which supported actual Sun4m SparcStations : Linux, NetBSD, OpenBSD, SunOS, Solaris, NextSTEP. Some OSes requires a special configuration.

SS20 seems to work with NetBSD with 3 CPUs. This is quite complex code and difficult to validate. Linux hardy ever supported multicore on these computers. I would like to be able to run multicore Solaris.
IIRC, the debug monitor (/soft/debugarm) is currently needed to properly activate SMP mode.
