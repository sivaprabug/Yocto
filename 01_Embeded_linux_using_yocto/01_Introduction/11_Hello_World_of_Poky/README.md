# Workflow of Yocto Project

Step 1: Download the Poky Source code

$ git clone git://git.yoctoproject.org/poky

Step 2: Checkout the latest branch/release (zeus)

$ git checkout zeus 

Step 3: Prepare the build environment

Poky provides you a script 'oe-init-build-env', which should be used to setup the build environment

script will set up your environment to use Yocto build system,including adding the BitBake utility to your path

$ source poky/oe-init-build-env [ build_directory ]

```shell
cd /home/weboe/siva/yocto/source/poky
source oe-init-build-env ../build
```
Here build_directory is an optional argument for the name of the directory where the environment is set

in case it is not given , it defaults to "build"

The above script will move you in a build folder and create two files ( local.conf, bblayers.conf ) inside conf folder

Step 4: Building Linux Distribution

$ bitbake <image_name>

```shell
time bitbake core-image-minimal

```
## core-image-minimal

This is a small image allowing a device to boot, and it is very useful for kernel and boot loader tests and development
