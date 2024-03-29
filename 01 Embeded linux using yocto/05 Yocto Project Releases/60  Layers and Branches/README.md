# Layers and Branches
---------------------

Layers being developed simultaneously by several different parties, the different flavors of Yocto and subsequent layers have to be split into branches in Git

Most BSP layers will only work with OpenEmbedded-Core of the same branch.

Mixing branches among your layers will end up in conflicts

For example, the so called bbappends, sometimes are tied to specific version number and will break the build if those versions are not found in the layers.

Which Branch to choose?
-------------------------

You should evaluate all the layers and find a compromise between:

    Getting the latest stable branch
    Getting the latest branch supported by all layers.

Note:  yocto branch you decided to use, could not be supported by your current host linux distribution.
Eg:  I want to use a layer which forces me to stick with Krogoth, but this branch is not tested with newer distributions such as Ubunutu 16.04 or 18.04.

