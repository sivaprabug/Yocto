# Booting Process in Raspberry Pi3

## Stage 2 Booting - bootcode.bin

- GPU - On, CPU - Off, SDRAM - On
- Executed on VideoCore GPU
- Enables SDRAM
- Loads the third stage bootloader start.elf into SDRAM

## Stage 3 Booting - start.elf

- GPU - On, CPU - On, SDRAM - On

- start.elf is actually a full fledge proprietary operating system for GPU known as VCOS (VideoCore OS).

- It starts by reading config.txt  which contains configuration parameters for

- VideoCore (Video/HDMI modes, memory, console frame buffers etc) and

- Linux Kernel (load addresses, device tree, uart/console baud rates etc)

- kernel = kernel7.img

- It also loads a file cmdline.txt if it exists, and will pass its contents as kernel command line

- Finally enables the ARM CPU and loads the kernel image which is executed on the ARM CPU

- It also loads the dtb file

## Booting in Raspberry Pi3

- GPU Core

- first stage bootloader, which is stored in ROM on the SoC

- bootcode.bin

- start.elf

- config.txt

- cmdline.txt

- kernel7.img
