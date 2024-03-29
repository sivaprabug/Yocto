# Exploring Build Folder

## conf

When you run source poky/oe-init-build-env, it will create a "build" folder in that directory
Inside this build folder, it will create "conf" folder which contains two files:

1. local.conf
2. bblayers.conf

## local.conf

Configures almost every aspect of the build system
Contains local user settings

MACHINE: The machine the target is built for
 Eg: MACHINE = "qemux86-64"

DL_DIR: Where to place downloads
 During a first build the system will download many different source code tarballs,from various
 upstream projects.These are all stored in DL_DIR
 The default is a downloads directory under TOPDIR which is the build directory

TMP_DIR:  Where to place the build output
   This option specifies where the bulk of the building work should be done and
   where BitBake should place its temporary files(source extraction, compilation) and output

```shell
siva@siva:~/project/yocto/build$ du -sh tmp/
27G tmp/
```

## Important Point

local.conf file is a very convenient way to override several default configurations over all the Yocto Project's tools.

Essentially, we can change or set any variable, for example, add additional packages to an image file

Though it is convenient, it should be considered as a temporary change as the build/conf/local.conf file is not usually tracked by any source code management system.
