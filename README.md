# Bride of Frankenstein
## Anycubic Kossel Linear Plus Refresh and Klipper Conversion

_Everything here is work in progress, but hopefully it can be of some help!_

This repo is a dump/backup of my current Anycubic Kossel Klipper configuration which I affectionately call:

**Bride of Frankenstein (_BOF_)**

After swapping out the main board a few times, cannibalizing parts, and losing my configs, I had to cobble this monster back into something usable.

My current goal is to produce a bill of materials so that this machine can be reproduced. I believe the original Anycubic KLP was a great starter delta machine and hope it continues to get some use!

In pursuit of that goal, I've added some hardware and printable mods that really improve the experience. I'll include the STLs, and I'll try to properly credit and source their creators later on. Thank you for your work!

I've included the current printer.cfg, custom macros (a few of which are adopted from people on the klipper discord / lots of googling), and my PrusaSlicer configs.

## CAD Attribution:

- [Original CAD by SPIKELEE](https://cults3d.com/:991294)

## STLs Attribution:

- [Improved Carriages (50mm version)](https://www.thingiverse.com/thing:2281894/files)
- [Upgraded Effector](https://www.thingiverse.com/thing:4329200)
- [Voron M4 Extruder](https://github.com/VoronDesign/Mobius-Extruder)
- [Glass Bed Clips](https://www.printables.com/model/137809-anycubic-kossel-linear-plus-glass-bed-clamp)
- [Regular Bed Clips](http://www.thingiverse.com/thing:2078581)
- [Corner Reinforcements](https://www.thingiverse.com/thing:2620272)
- [Top Mount Tensioners](https://www.thingiverse.com/thing:2827665)
- [Side Mounted Spool Holder](https://www.thingiverse.com/thing:2909802)



## Mods Currently in Use:

- [TMC2209s](https://www.amazon.com/BIGTREETECH-TMC2209-Stepper-Stepstick-Motherboard/dp/B07ZPYKL46/ref=sr_1_3?keywords=tmc2209&qid=1696062611&sr=8-3&th=1) _(I might post a guide for this since the resources I used in the past are outdated)_
- E3D V6 Clone _(Gulfcoast Robotics)_
- [Ultrabase](https://www.aliexpress.us/item/2251832729128038.html?gatewayAdapt=glo2usa4itemAdapt) _(I DO NOT recommend this bed, but it is currently what I am using. Adhesion sucks)_

## Macros worth pointing out:

- [PURGE_ARC](https://github.com/whyme12/Klipper_Macro_Collection)
- M600 _(If I can find the source I'll link it)_

## A few issues to note:

*Due to the modified effector I am currenty using, you can't use the fully radius of the build area. It's currently locked at R100mm for the Delta Radius, but delta calibrate says it's 134mm. To compensate, my PrusaSlicer profile is locked at D200mm. Also the PURGE_ARC macro has a 35mm offset to not exceed max dimensions.*

*Retraction is a bit out of whack at the moment. Currently running an Voron Mobius 4 Extruder on the worlds worst nema 17 (ripped from a tevo tarantula). My accel values are a bit off to not generate too much noise while printing. Although, I may try to drop retract speed even further. Update: I ran a slow retraction test. I believe the issue to actually be pressure advance. The filament travel is quite long so my PA values are really aggressive. I'll shorten it and retune.* 

*Tip: Something I learned the hard way is that you CANNOT use BED_MESH_CALIBRATE while running DELTA_CALIBRATE. Delta calibrate compensates for any innacuracies in your build by assuming a planar build surface. This means running a bed mesh will just exagerate imperfections and wildly throw off kinematics. (I've literally watched the effector fly away from the bed on the first layer)*
