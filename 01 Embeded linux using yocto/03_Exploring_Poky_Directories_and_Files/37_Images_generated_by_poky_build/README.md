# Images generated by poky build

The build process writes images out to the Build Directory inside the tmp/deploy/images/machine/ folder

1. kernel-image:

A kernel binary file

The KERNEL_IMAGETYPE variable determines the naming scheme for the kernel image file.

```shell
$ bitbake -e core-image-minimal | grep ^KERNEL_IMAGETYPE=
```

2. root-filesystem-image: 
Root filesystems for the target device (e.g. *.ext3 or *.bz2 files).

The IMAGE_FSTYPES variable determines the root filesystem image type
```shell
$ bitbake -e core-image-minimal | grep ^IMAGE_FSTYPES=
```

3. kernel-modules:

Tarballs that contain all the modules built for the kernel

4. bootloaders:

If applicable to the target machine, bootloaders supporting the image.

symlinks

- symbolic link pointing to the most recently built file for each machine

- These links might be useful for external scripts that need to obtain  latest version of each file
