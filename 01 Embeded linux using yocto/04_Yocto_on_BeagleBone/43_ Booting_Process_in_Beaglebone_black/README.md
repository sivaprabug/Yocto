# Booting Process in Beaglebone black

        The first stage bootloader is flashed in ROM on the device by Texas Instruments.

The ROM code is the first block of code that is automatically run on device start-up or after power-on reset (POR)

The ROM bootloader code is hardcoded into the device and cannot be changed by the user.

The ROM code has two main functions:

-Configuration of the device and initialization of primary peripherals
	Stack setup
	Configure Watchdog Timer 1 (set to three minutes)
	PLL and System Clocks configuration

- Ready device for next bootloader
	Check boot sources for next bootloader (SPL)
	Moves next bootloader code into memory to be run

The main purpose of the ROM code is to set up the device for the second stage bootloader.

By default, the ROM code in the Sitara AM3359 will boot from the MMC1 interface first (the onboard eMMC), followed by MMC0 (external uSD), UART0 and USB0.

If the boot switch (S2) is held down during power-up, the ROM will boot from the SPI0 Interface first, followed by MMC0 (external uSD), USB0 and UART0.
