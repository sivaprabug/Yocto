# What is Class?

Class files are used to abstract common functionality and share it amongst multiple recipe (.bb) files

To use a class file, you simply make sure the recipe inherits the class

Eg. inherit classname

Extension: .bbclass

They are usually placed in classes directory inside the meta* directory

Example of classes

cmake.bbclass - Handles cmake in recipes
kernel.bbclass - Handles building kernels. Contains code to build all kernel trees
module.bbclass - Provides support for building out-of-tree Linux Kernel Modules