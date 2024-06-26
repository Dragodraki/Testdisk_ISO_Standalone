# Testdisk_ISO_Standalone
Allows to boot pure Testdisk-DOS from BIOS (~~UEFI~~ CSM) - 3 MB Image
<br/>
Alternatively use Testdisk-WinPE from BIOS or UEFI - 634 MB Image

Testdisk is a reliant software to recover lost partitions or try to repair its table when boot errors appear (if not encrypted or depth erased), may it originated by defect disk sectors (hardware) or manipulated MBR aka master-boot-recored (software) as long the data is not encrypted/unreadable/overwritten. If you use Bitlocker or other disk encryption : forget it (no chance!).
Version 7.2 seeems to be the latest (and last) release from 2024. The publisher provided it as windows app (.exe) and part of other images like Cygwin.
But he never bothered to offer a direct ISO-image without the unnecessary elements.
<br/>

If you explicit need Testdisk on UEFI-only systems or would like to have command prompt, registry and PhotoRec onboard too, take this 3rd party Testdisk-WinPE instead. I am neither liable for any damage you might do with it nor support any bugs since this is a reference link only.

<br/>

|           | Testdisk-DOS (mine) | Testdisk-WinPE (3rd party) |
:-------------------------:|:-------------------------:|:-------------------------:
Download | [<img src="https://user-images.githubusercontent.com/76787321/197257488-1b7aa8e9-9b6f-4600-949e-8ff477cb4bf4.png" width="40%"></img>](https://github.com/Dragodraki/Testdisk_ISO_Standalone/releases/latest/download/Testdisk_7.2.iso) | [<img src="https://private-user-images.githubusercontent.com/76787321/343722421-9c77f5f7-62d1-4324-b132-2597dadf3f29.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk0ODE5OTUsIm5iZiI6MTcxOTQ4MTY5NSwicGF0aCI6Ii83Njc4NzMyMS8zNDM3MjI0MjEtOWM3N2Y1ZjctNjJkMS00MzI0LWIxMzItMjU5N2RhZGYzZjI5LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA2MjclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwNjI3VDA5NDgxNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWU5YTkzMmZlMmNmODYyZmQ2NzliNGU1ZDU4ODBlMWVmY2U3ZTZmNzllMTNkYmYyZjYyOGM1OTY2MTdiZWExYjYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.ejW7FV4bA4RirVj7POOhhYVHiHBVoILsNBVD-UHOYuA" width="40%"></img>](https://downloads.sourceforge.net/project/testdisk-pe.testdisk.p/TestDisk%20PE_x64.iso?ts=gAAAAABmfTYdMBfgA6C0krutWApjenymWixIaJFaGAeuhHE_JD3a5hgtIdxmhzq5fmqnavmDo8MhhvZchgLA5BA8BW72_C8qDw%3D%3D&r=https%3A%2F%2Fsourceforge.net%2Fprojects%2Ftestdisk-pe.testdisk.p%2Ffiles%2FTestDisk%2520PE_x64.iso%2Fdownload%3Fuse_mirror%3Dliquidtelecom%26r%3D)
Version | 7.2 Stable (2024) | 7.2 Beta (2019) |
Motherboard | BIOS/CSM only | Both UEFI & BIOS/CSM |
Filesize | 3 MB | 634 MB |
Booting speed | 1-2 secconds | about 30 secconds |
Architecture | x86 (32 bit) | x64 (64bit) |
Other tools | Testdisk | Testdisk<br/>PhotoRec<br/>Command Prompt<br/>Registry Editor<br/>MultiCommander |
<br/>

Important:
Do not use the integrated command prompt in Testdisk WinPE version for manual/automatic startup repair for Windows Vista/7/8, as this WinPE based on Windows 10 many utils like bootrec.exe, bcdboot.exe and some others would mess up with any other than Windows 10 (and maybe Windows 11) or simply not work. I tested it myself: Only if using the appropriate general Windows ISO that matches your windows version the commands with bootrec.exe and bcdboot.exe were able to repair Windows. That means - please use Windows 7 ISO to repair Windows Vista/7, Windows 8 ISO to repair Windows 8, Windows 10/11  ISO to repair Windows 10/11.

<br/>

-------------------------------
USAGE
-------------------------------

Here you go with Testdisk ISO file:

a) For USB: You need an empty flash drive and a tool like "Rufus" or "Easy2Boot" to get it to work on a USB.

b) For CD (DVD/BD): You need a empty writable disc, a data-disc-drive and a tool like "ImgDrive" or "CDBurnerXP" to burn it.

Important:
Due to DOS limitation the DOS-version it is absolutely incompatible with UEFI-only boot mode! Your computer needs a motherboard (that supports) having Legacy/BIOS boot mode enabled to enter Testdisk for DOS. This cannot be changed, I wasted much time by trying so - its in vain (UEFI simply sucks in my opinion). Solution: Use Testdisk-WinPE then instead.

-> Put the disc/flash in your pc, disable secure boot in bios (if enabled) and press boot keyboard key (mostly F11/F12/ESC) to boot it. Press ENTER when asked whether you'l like to continue - testdisk is loaded. Note: As typical for DOS environment, keyboard inputs are supported only (no use of mouse possible).


-------------------------------
LICENSE
-------------------------------

Legal distribution:
Testdisk originally is Open-Source. So my improved modification of it will be too. You are allowed to share/copy it in the same way its publisher allowed it. That does not apply for the DOS/Microsoft system files, but is limited to Testdisk only. One request: If you plan to fork my Testdisk-DOS versioned ISO, feel free to do so, but you have to name me as original programmer for the mod in your readme!
