# Mambui Homepage

To be installed on Raspbian Jessie. Project files can also be cloned into a FullPageOS installation.

## Installation steps:
```
wget https://dl.dropboxusercontent.com/u/87113035/chromium-browser-l10n_45.0.2454.85-0ubuntu0.15.04.1.1181_all.deb
wget https://dl.dropboxusercontent.com/u/87113035/chromium-browser_45.0.2454.85-0ubuntu0.15.04.1.1181_armhf.deb
wget https://dl.dropboxusercontent.com/u/87113035/chromium-codecs-ffmpeg-extra_45.0.2454.85-0ubuntu0.15.04.1.1181_armhf.deb
sudo dpkg -i chromium-codecs-ffmpeg-extra_45.0.2454.85–0ubuntu0.15.04.1.1181_armhf.deb
sudo dpkg -i chromium-browser-l10n_45.0.2454.85–0ubuntu0.15.04.1.1181_all.deb chromium-browser_45.0.2454.85–0ubuntu0.15.04.1.1181_armhf.deb
sudo apt-get install x11-xserver-utils
cd .config/lxsession/LXDE-pi/
sudo nano autostart
```
Add this to the end: 
```
@chromium-browser — kiosk — incognito /home/pi/GEC-2017-Site-Concept/index.html
@xset s noblank
@xset s off
@xset -dpms
```
Save with Ctrl+X.
```
sudo nano /etc/lightdm/lightdm.conf
```
Change the line beginning with xserver-command to read like this:
```
xserver-command= X -s 0 -dpms
```

## Credits

Thank you to Mike Swartz of Upstatement for the **[guide](https://medium.com/stories-from-upstatement/how-to-build-a-web-kiosk-with-a-raspberry-pi-some-cables-and-a-tv-3dc2724acaa1#.aedvwj5jg)** on how to install this on a Raspberry Pi.

Start Bootstrap and the Freelancer theme were created by and are maintained by **[David Miller](http://davidmiller.io/)**, Owner of [Blackrock Digital](http://blackrockdigital.io/).

* https://twitter.com/davidmillerskt
* https://github.com/davidtmiller

Start Bootstrap is based on the [Bootstrap](http://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).

## Copyright and License

Copyright 2013-2016 Blackrock Digital LLC. Code released under the [MIT](https://github.com/BlackrockDigital/startbootstrap-freelancer/blob/gh-pages/LICENSE) license.
