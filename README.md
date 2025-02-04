## HackSL500, my Lenova SL500 i3wm setup


### Programs
| category       | name                                |
|----------------|:-----------------------------------:|
| window manager | i3                                  |
| bar            | i3blocks                            |
| launcher       | rofi                                |
| notifications  | dunst                               |
| composer       | picom                               |
| browser        | firefox               			       |
| terminal       | sakura                              |
| file manager   | joshuto                             |
| image viewer   | feh                                 |
| wallpapers     | nitrogen                            |
| theme          |                                     |
| icons          |                                     |
| fonts          | [Hack Nerd Fonts](https://www.nerdfonts.com/)  |
| cursor         |                                     |
| music player   | moc, [pmrp](https://github.com/hakerdefo/pmrp) |
| video player   | mpv                                 |
| screenshots    | flameshot                           |
| text editor    | nvim, kakoune                       |
| bluetooth      | blueberry                           |
| appstore       |                                     |
| ssh		 | mosh				                                 |
| pdf		 | zathura			                               |


### Installation

### Place of configurations
```
i3 -> ~/.config/i3/
```
### Notes

1. I salvaged an old Lenova SL500 running AntiX (Debian based) from a friend after my main machine was water-damaged.
   
2.  I setup an earlier version HackPi on Raspberry 3B+ during a level 9 storm in Cape Town. During a disaster, the only thing you may have, is a late model Raspberry Pi. Crucial to have a setup that will actually work on the Net.

3. Mods to SL500: Upgrade Bios from 18 to 30, upgrade ram 1Gb > 4Gb, move sata drive to dvd drive bay using a TISHRIC caddy. Replace sata main drive with 100Gb ssd.

4. Convert bios iso to img, then move img to usb stick and boot.
```
sudo apt-get install genisoimage
geteltorito -o bios.img bios.iso
```
or
```
geteltorito f1.iso > f1.img
```

Then copy to the USB key:

```
sudo fdisk -l /dev/sdb  # double check that the device is right
sudo dd if=bios.img of=/dev/sdb #Will Erase the drive!! 
```
see:[Write bootable BIOS update .ISO to USB stick](https://askubuntu.com/questions/651281/write-bootable-bios-update-iso-to-usb-stick)
