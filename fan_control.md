Now we can not set cpu fan speed or edit the temperature curve because the bios locked.
TIMI TM1707 XMAKB5RRP0804

Do not use utils like NBFC because this may break the charging port.

Charging is stopped, blinking red light:
`sudo systemctl stop nbfc`
`sudo systemctl disable nbfc`
`sudo pacman -R nbfc`
