# OpenCore EFI for ASRock X570 Creator - AMD Hackintosh - BIG SUR - OpenCore 6.6

Thunderbolt works on cold start,  at least one of them does, bluetooth works all the time

  
I have a SAPPHIRE NITRO+ RX VEGA64 8G HBM2 graphics card and therefore only this SSDT  in ACPI 
The other graphics drivers I removed

corpnewt's USBMap tool seems to be very good, https://github.com/corpnewt/USBMap Im trying to work out how to clean out  my SSTD´s using this tool

***v066 - 2021-02-05***

***BT/WiFi Updates -  2021-02-05**


## A. Contents

### 1. ACPI

Cold start mounts the 2big Dock Thunderbolt™ 3 drives
I use the built in BlueTooth from motherboard
I use the built in WiFi from motherboard


### 2. Kexts

I added OpenIntelWireless  https://github.com/OpenIntelWireless  Heliport itlwm and IntelBluetoothFirmware
I added https://github.com/trulyspinach/SMCAMDProcessor and AMD.Power.Gadget.app
Trying to remove or update more kexts lets se how that goes


### 3. BT Settings
Both bluetooth from motherboard works, but I find It is harder to connect mac keyboard and trackpad, also uses juice from trackpad in 1 -2 days
Got an IOGEAR Bluetooth 4.0 USB Micro Adapter witch works fine, and connects automaticly on boot with kb and trp.   When using this I disable bluetooth radio in BIOS.


### 5. Drivers
Removed some of them


### 7. BIOS ROM
2.1 works
2.4 works
2.7 panic  somthing to do with nvram or lack of..   investigating
3.0 panic  somthing to do with nvram or lack of..   investigating
3.1 panic  somthing to do with nvram or lack of..   investigating
3.2 not tested


### 8. BIOS Settings

Turned off the above 4G dedoding and putin boot-args   npci=0x2000 


## E. Discussion

https://forum.amd-osx.com/index.php?threads/big-sur-on-x570-creator-sleep-wake-works.815/

https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/



### Credits
CaseySJ   https://forum.amd-osx.com/index.php?threads/big-sur-on-x570-creator-sleep-wake-works.815/
https://www.tonymacx86.com/members/caseysj.2134452/
https://www.tonymacx86.com/search/6720387/?q=ASRock+X570+Creator&c[users]=CaseySJ&o=date

    - [AlGrey](https://github.com/AlGreyy) for the idea and creation of the AMD [patches](https://github.com/AMD-OSX/AMD_Vanilla/tree/opencore)
    - [AMD OS X](https://github.com/AMD-OSX/AMD_Vanilla/tree/master) for AMD related information
    - [CaseySJ](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/) for tireless work and ingenuity in TB decoding
    - [Download-Fritz](https://github.com/Download-Fritz) for OpenCore
    - [Hackintool](https://www.insanelymac.com/forum/topic/335018-hackintool-v286/) for Hackintool utility
    - [Kext Updater](https://bitbucket.org/profdrluigi/kextupdater/downloads/) for Kext Updater utility
    - [khronokernel](https://khronokernel.github.io/Opencore-Vanilla-Desktop-Guide/) for a great OC guidebook
    - [NDK OC Menu](https://github.com/n-d-k/NdkBootPicker) for NDKBootPicker Menu for OC
    - [Pavo](https://github.com/Pavo-IM) for OCBuilder and AGPMInjector
    - [CorpNewt](https://github.com/corpnewt) for many things such as GenSMBIOS and ProperTree editor
    - [trulyspinach](https://github.com/trulyspinach/SMCAMDProcessor) for CPU Temp/Freq monitoring
    - [vit9696](https://github.com/vit9696) for OpenCore and many of the kexts we use
