# Bitbake

Bitbake is a core component of the Yocto Project.

It basically performs the same functionality as of make.

It's a task scheduler that parses python and shell script mixed code

The code parsed generates and runs tasks, which are basically a set of steps ordered according to code's dependencies.

It reads recipes and follows them by fetching packages, building them and incorporating the results into bootable images.

It keeps track of all tasks being processed in order to ensure completion, maximizing the use of processing resources to reduce build time and being predictable.