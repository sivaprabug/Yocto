# Steps for building

Step1 : Source the environment script

```shell
source poky/oe-init-build-env
```

Add the meta-ti layer

```shell
bitbake-layers add-layer ~/Yocto_Training/source/meta-ti/
```

Step2 : Open local.conf and set Machine to beaglebone

MACHINE='beaglebone'

Step3 : Also add INHERIT += "rm_work" to save disk space

Step4 : Generate an minimal image

```shell
bitbake core-image-minimal
```

Step5 : Once the build finished, you will find the output images under

```shell
BUILDDIR/tmp/deploy/images/beaglebone  
```
