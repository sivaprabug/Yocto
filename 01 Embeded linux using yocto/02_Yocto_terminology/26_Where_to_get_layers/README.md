# Where to get layers?

# Find out layers used by bitbake build system

Which layers are used by Poky Build System ?

BBLAYERS variable present in build/conf/bblayers.conf file list the layers Bitbake tries to find

If bblayers.conf is not present when you start the build, the OpenEmbedded build system creates it from bblayers.conf.sample 

when you source the oe-init-build-env script

Command to find out which layers are present

$ bitbake-layers show-layers

Note: You can include any number of available layers from the Yocto Project

Where to get other layers

https://layers.openembedded.org/layerindex/branch/master/layers/