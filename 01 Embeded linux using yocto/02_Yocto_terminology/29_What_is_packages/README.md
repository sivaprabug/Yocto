# What is Packages?

Non-Yocto: Any wrapped or boxed object or group of objects.

Yocto: A package is a binary file with name *.rpm, *.deb, or *.ipkg

A single recipe produces many packages.

All packages that a recipe generated are listed in the recipe variable

$ vi meta/recipes-multimedia/libtiff/tiff_4.0.10.bb

PACKAGES =+ "tiffxx tiff-utils"