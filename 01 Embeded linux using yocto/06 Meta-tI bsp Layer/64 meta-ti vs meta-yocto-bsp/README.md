# meta-ti vs meta-yocto-bsp

## meta-yocto-bsp:
---------------

    provides "reference" BSPs for each of the supported architectures
    One for ARM (BeagleBone Black), one for MIPS, PPC and x86.
    it is based on the mainline kernel/bootloader
    does not support any advanced features or anything not in the upstream mainline kernel
    e.g. no capes, no power management, no hardware acceleration, no 3D, no PRU, etc.
    The purpose of this BSP is to have some basic out-of-box experience for the select hardware platforms within Poky to evaluate the Yocto Project and OpenEmbedded framework, but not the specific hardware platforms

## meta-ti
    official Texas Instruments BSP that provides the latest WIP "staging" kernel and bootloader
    most of the advanced features and peripheral support for the wider range of latest TI platforms

