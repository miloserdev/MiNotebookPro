Now we can not edit the temperature curve because the bios locked.
TIMI TM1707 XMAKB5RRP0804
  
#WARNING!  
##THIS MAY BRICK YOUR LAPTOP IF TYPE WRONG REGISTER!  
First stop nbfc service then  
type `sudo ec-probe write 0xA0 0xFF` - set left fan speed to max  
type `sudo ec-probe write 0xCB 0xFF` - set both fans speed to max (works if 0xA0 is not set)  
0xCB - 0x11 to return both fans
