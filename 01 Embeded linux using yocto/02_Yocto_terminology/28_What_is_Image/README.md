# What is Image?

An image is the top level recipe, it has a description, a license and inherits the core-image class

It is used alongside the machine definition

machine describes the hardware used and its capabilities

image is architecture agnostic and defines how the root filesystem is built, with what packages.

By default, several images are provided in Poky

Command to check the list of available image recipes

$ ls meta*/recipes*/images/*.bb