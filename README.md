# AMD_OC_Ryzen

This commit provides the basic contents for an EFI folder to successfully boot an ASRock X570 Creator motherboard,
using a Ryzen 9 CPU such as a 3950X.

There are notable dependencies on OpenCore, the suggested bootloader. OpenCore is best updated via Pavo's OCBuilder app
(https://github.com/Pavo-IM/ocbuilder/releases). Accordingly, specific files compiled during an OC build will not be 
necessarily updated in this repository.

For details regarding how to setup OpenCore, how to create a bootable installation, how to trouble shoot errors,
how to optimize your sysstem and so forth, please see AMD-OSX/AMD-Vanilla repository at 
https://github.com/AMD-OSX/AMD_Vanilla/tree/master. This repository will not go into such details, but rather
will attempt to keep an up-to-date EFI that works on an established computer.

Presently, TB3 while working, is still incomplete. Check discusson sites listed below. 

##Usage:
 
- To build OpenCore using Pavo's OCBuilder. It is recommended to use the Release version.
- Move included folders for ACPI, Drivers, Kexts and config.plist files into EFI/OC folder created by OCBuilder
- Final EFI folder should have a structure like this (as of OC version 056:

       EFI----Boot----Bootx64.efi
        |
        |_____OC_____ACPI
               |       |____various *.aml files
               |
               |_____config.plist
               |
               |_____config-Only-For-Storage.plist
               |
               |_____Docs
               |       |_____AcipSamples
               |       |          |_______various SSDT files
               |       |
               |       |_____Changelog.md, Configuration.pdf, Differences.pdf, Sample.plist, SampleFull.plist
               |
               |_____Drivers
               |       |______ApfsDriverLoader.efi, AudioDxe.efi, FwRuntimeServices.efi, HFSPlus.efi
               |
               |_____Kexts
               |       |______various *.kext files
               |
               |_____OpenCore.efi
               |
               |_____Resources
               |       |_____Audio
               |                |____ various WAV files
               |_____Tools
               |       |______BootKicker.efi, CleanNvram.efi, GopStop.efi, HdaCodecDump.efi, Shell.efi, VerifyMsE2.efi
               |
               |_____Utilities
                       |_____BootInstall
                       |
                       |_____CreateVault
                       |
                       |_____LogoutHook
                      
                      
 -This commit contains only the ACPI, Driver and Kexts folders along with the config.plist and config-Only-For-Storage.plist
    files.
 -Once in use, the Driver and Kext folders can be updated outside this commmit by running OCBuilder and transferring the
    appropriate, newly udpated files to their respective folders.
    
    

## Discussion

- [forum.amd-osx](https://forum.amd-osx.com/viewtopic.php?f=35&t=9645) especially for TB3 updates



## Credits

- [AlGrey] (https://github.com/AlGreyy)for the idea and creating the patches
- [Andrey1970AppleLife](https://github.com/Andrey1970AppleLife)
- [AMD OS X](https://github.com/AMD-OSX/AMD_Vanilla/tree/master)
- [Download-Fritz](https://github.com/Download-Fritz)for OpenCore
- [trulyspinach](https://github.com/trulyspinach/SMCAMDProcessor)for CPU Temp/Freq monitoring
- [vit9696](https://github.com/vit9696)for OpenCore and many of the kexts we use
