# Second Stage Bootloader: SPL

A fully featured version of U-Boot can be over 400KB, and the internal RAM on the AM335X is 128KB

Hence it is not possible to load this immediately

For this reason, a cut down version of U-Boot called U-Boot SPL (Second Program Loader) is loaded first,

once it has initialised the CPU, it chain loads a fully featured version of U-Boot (u-boot.img).

Name of SPL should be MLO

It should be located on active first partition of MMC, which must be formatted as FAT12/16/32
