# BrideOfFrankenstein
## Anycubic Kossel Linear Plus Klipper Conversion

This repo is a dump/backup of my current Anycubic Kossel Klipper configuration which I affectionately call:
Bride of Frankenstein.

After swapping out the main board a few times and losing my configs, I had to start from scratch.

I've included the current printer.cfg, my custom macros (a few of which are adopted from people on the klipper discord), and I'll soon add my PrusaSlicer configs.

## A few issues to note:

*Due to the modified effector I am currenty using, you can't use the fully radius of the build area. It's currently locked at R100mm for the Delta Radius, but delta calibrate says it's 134mm. To compensate, my PrusaSlicer profile is locked at D200mm. Also the PURGE_ARCH macro has a 35mm offset to not exceed max dimensions.*

*Retraction is a bit out of whack at the moment. Currently running an Voron Mobius 4 Extruder on the worlds worst nema 17 (ripped from a tevo tarantula). My accel values are a bit off to not generate too much noise while printing.* 
