# Four elements of embedded Linux

## Toolchain:

The compiler and other tools needed to create code for your target device. Everything else depends on the toolchain.

## Bootloader:

The program that initializes the board and loads the Linux kernel.

## Kernel:

This is the heart of the system, managing system resources and interfacing with hardware.

## Root filesystem:

Contains the libraries and programs that are run once the kernel has completed its initialization.

One more element can be collection of programs specific to your embedded application which make the device do whatever it is supposed to do, be it weigh groceries, display movies, control a robot, or fly a drone.