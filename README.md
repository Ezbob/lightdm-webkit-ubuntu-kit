# lightdm-webkit-ubuntu-kit
A lightdm greeter webkit theme for ubuntu machines based on the archlinux greeter theme: [lightdm-webkit-archlinux-theme](https://github.com/shosca/lightdm-webkit-archlinux-theme) which again is based on [LightDM-Webkit-MacOSX-Theme](https://github.com/Wattos/LightDM-Webkit-MacOSX-Theme), so thanks to them!
## Installation 
This guide assumes that you're using a Ubuntu distrobution or some distrobution that uses `apt`.

You first need to install lightdm-webkit edition:
```sh
sudo apt-get install lightdm-webkit-greeter
```
Then copy the `ubuntu-kit` folder to (remember to `sudo` this):
```
/usr/share/lightdm-webkit/themes/
```
Then in `/etc/lightdm/` edit/create file `lightdm.conf` and put in the lines:
```
[SeatDefaults]
greeter-session=lightdm-webkit-greeter
```
to setup lightdm to use the webkit version of lightdm. 
Finally, in the same folder edit/create file `lightdm-webkit-greeter.conf` (don't forget to back it up!) and put in the lines:
```
[greeter]
webkit-theme=ubuntu-kit
```
This should set `lightdm-webkit` to use the new theme.

You probably need to reboot now.

Enjoy!

### Troubles
#### Getting a awful white background
Lightdm may not have the right permissions to show them; go to the `ubuntu-kit` and `chmod -R 644` on the `img` folder. This should set the right permissions to the images used by this theme.
#### Man, it's ugly
Yeah, well.. Fork it, and do it better youself or just don't use it! ;-)
