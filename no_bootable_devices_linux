If you see No Bootable Devices display when running.
One of reasons is selecting Legacy mode then switch back to UEFI mode.


1. First make a usb with linux setup utility
2. Switch BOOT Mode to UEFI
3. Plug usb and reboot
  (if linux setup is not started automatically, press F12 at start then select your usb drive with linux setup utility)

4. type `fdisk -l` and you will see
  Device           Start       End   Sectors  Size Type
  /dev/nvme0n1p1    2048     65535     63488   31M BIOS boot
  **/dev/nvme0n1p2   65536   1089535   1024000  500M EFI System**
  /dev/nvme0n1p3 1089536 500118158 499028623  238G Linux filesystem

5. Mount the device that contains EFI System type (in this case - /dev/nvme0n1p2)
  mount /dev/nvme0n1p2 /mnt
  
6. type `cd /mnt` and `ls`
  There is EFI directory
  type `cd EFI`
  In this case we have **arch** directory that contains grubx64.efi
  type `mkdir BOOT` `cp /arch/grubx64.efi /BOOT/`

7. type `cd /` then `umount /dev/nvme0n1p2`
8. type `reboot`, now you can unplug the usb, then press F12 on startup and select your drive/
