# Testdisk_ISO_Standalone
Allows to boot pure Testdisk-DOS from BIOS (~~UEFI~~ CSM) - 3 MB Image

Testdisk is a reliant software to recover lost partitions or try to repair its table when boot errors appear (if not encrypted or depth erased).
Version 7.2 seeems to be the latest (and last) release from 2024. The publisher provided it as windows app (.exe) and part of other images like Cygwin.
But he never bothered to offer a direct ISO-image without the unnecessary elements.
<br/>

[<img src="https://user-images.githubusercontent.com/76787321/197257488-1b7aa8e9-9b6f-4600-949e-8ff477cb4bf4.png" width="23%"></img>](https://github.com/Dragodraki/Testdisk_ISO_Standalone/releases/latest/download/Testdisk_7.2.iso)

<br/>

-------------------------------
USAGE
-------------------------------

Here you go with Testdisk 7.2 as 3 megabyte size ISO file:

a) For USB: You need an empty flash drive and a tool like "Rufus" or "Easy2Boot" to get it to work on a USB.

b) For CD (DVD/BD): You need a empty writable disc, a data-disc-drive and a tool like "ImgDrive" or "CDBurnerXP" to burn it.

Important:
Due to DOS limitation it is absolutely incompatible with UEFI-only boot mode! Your computer needs a motherboard (that supports) having Legacy/BIOS boot mode enabled to enter Testdisk for DOS. This cannot be changed, I wasted much time by trying so - its in vain (UEFI simply sucks in my opinion).

-> Put the disc/flash in your pc, disable secure boot in bios (if enabled) and press boot keyboard key (mostly F11/F12/ESC) to boot it. Press ENTER when asked whether you'l like to continue - testdisk is loaded. Note: As typical for DOS environment, keyboard inputs are supported only (no use of mouse possible).


-------------------------------
LICENSE
-------------------------------

Legal distribution:
Testdisk originally is Open-Source. So my improved modification of it will be too. You are allowed to share/copy it in the same way its publisher allowed it. One request: If you plan to fork my ISO, feel free to do so, but you have to name me as original programmer for the mod in your readme!
