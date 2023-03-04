# Steps to generate ARM image and run in QEMU

When you set up the build environment, a local configuration file named local.conf becomes available in a conf subdirectory of the Build Directory

The defaults are set to build for a qemux86-64 target

Edit ./build/conf/local.conf

Set

MACHINE = "qemuarm"

$ source poky/oe-init-build-env

$ bitbake core-image-minimal

$ runqemu core-image-minimal