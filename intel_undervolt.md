**Linux version**
How to undervolt CPU on bios TIMI TM1707 Xiaomi Mi Notebook Pro GTX 1050

1. Download /Tools/bootx64.EFI
2. Pick usb flash drive then `mkdir EFI`, `cd EFI`, `mkdir BOOT`
3. `cp bootx64.EFI` into `BOOT` dir
4. Reboot and type F2 on startup then select usb flash as boot device
5. You will see **grub>** shell
	5.1 type `setup_var_cv CpuSetup 0x3C 0x1 0x0` - CFG Lock
        5.2 type `setup_var_cv PchSetup 0x17 0x1 0x0` - BIOS Lock
        5.3 type `setup_var_cv CpuSetup 0xEB 0x1 0x0` - Overclocking Lock
6. Reboot and unplug usb flash drive
7. Install linux-undervolt package
8. type `sudo ${youreditor} /etc/intel-undervolt.conf`
	8.1 Change `undervolt` parameters like this (i really recommend use this config)

	undervolt 0 'CPU' -105.50
	undervolt 1 'GPU' -80.10
	undervolt 2 'CPU Cache' -105.50
	undervolt 3 'System Agent' 0
	undervolt 4 'Analog I/O' 0
9. type `sudo intel-undervolt apply``




===================================================================================




**Windows version**

1. Go to [Wiki](https://wiki.archlinux.org/title/installation_guide)
2. Click `Download`
3. Then install Linux)
