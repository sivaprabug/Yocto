# Booting Process in Raspberry Pi3

Broadcom BCM2837:

- CPU  - 1.2GHz 64-bit quad-core ARMv8 Cortex-A53
- GPU  - Broadcom VideoCore IV
- SDRAM - 1024 MiB

When you power the device

## Stage 1 Booting - OnChip ROM

- GPU - On, CPU - Off, SDRAM - Off

- When the Pi is powered up the first thing that starts working is the GPU core and ARM CPU is held in reset

- The GPU core is the main part responsible for the first booting steps of the Pi.

- Inside Broadcom’s SoC, there is a small boot ROM, its programmed by default to look for a file called
bootcode.bin on the SD Card

- It loads bootcode.bin into L2 Cache memory
