JBTEK 3.5" LCD Device Tree Overlay for the Raspberry PI
===
This is an Overlay I wrote that supports the [JBTek 3.5" TFT LCD](http://www.amazon.com/JBtek-Version-480x320-Raspberry-Nov-2014/dp/B00OB0S8KE) for the Raspberry PI and PI 2 using [notro](https://github.com/notro)'s FBTFT driver.

Installation
===
1. Follow the steps on [notro's wiki](https://github.com/notro/fbtft/wiki#install) for installing the fbtft driver on your pi/pi2 (Your PI will not boot with the LCD attached until the right overlay is specified in /boot/config.txt)
2. Clone my repo onto your pi
```shell
git clone git@github.com:acidjazz/jbtekoverlay.git
```
2. Copy my overlay file `jbtek-overlay.dtb` to `/boot/overlays` as root
```shell
sudo cp jbtekoverlay/jbtek-overlay.dtb /boot/overlays/.
```
3. Specify this overlay file in your `/boot/config.txt` along with activating SPI
```ini
dtparam=spi=on
dtoverlay=jbtek
```
4. reboot your raspberry pi

