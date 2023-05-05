Command to run the generated image in QEMU
==========================================

Quick Emulator ( QEMU ) is a free and open source software package that performs hardware virtualization.

The QEMU based machines allow test and development without real hardware.

Currently emulations are supported for:
        • ARM
        • MIPS
        • MIPS64
        • PowerPC
        • X86
        • X86_64


Poky provides a script 'runqemu' which will allow you to start the QEMU using yocto generated images.

The runqemu script is run as:

   runqemu <machine> <zimage> <filesystem>
```shell
cd /home/weboe/siva/yocto/source/build$
../poky/scripts/runqemu qemux86-64 core-image-minimal

```
where:

   <machine> is the machine/architecture to use (qemuarm/qemumips/qemuppc/qemux86/qemux86-64)
   <zimage> is the path to a kernel (e.g. zimage-qemuarm.bin)
   <filesystem> is the path to an ext2 image (e.g. filesystem-qemuarm.ext2) or an nfs directory

Full usage instructions can be seen by running the command with no options specified.

Exit QEMU
-----------

Exit QEMU by either clicking on the shutdown icon or by typing Ctrl-C in the QEMU transcript window from which you evoked QEMU.
