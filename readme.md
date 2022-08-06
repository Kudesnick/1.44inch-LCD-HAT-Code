# 1.44inch-LCD-HAT

Original instruction: https://www.waveshare.com/wiki/1.44inch_LCD_HAT
Original code: https://www.waveshare.com/w/upload/f/fa/1.44inch-LCD-HAT-Code.7z

Tested on Raspberry Pi Zero W.

## Python example

1. Enable SPI interface:
~~~
# sed -i "s/#dtparam=spi=on/dtparam=spi=on/" "/boot/config.txt"
# reboot
~~~

2. Install python packages:
~~~
# apt install python3-numpy
# pip install python3-pil
~~~

3. Download code:
~~~
$ git clone https://github.com/kudesnick/1.44inch-LCD-HAT-Code.git
~~~

4. Run test:
~~~
$ cd 1.44inch-LCD-HAT-Code/python/
$ python main.py
~~~

## Device tree overlay

1. dt overlay test:
~~~
$ cd 1.44inch-LCD-HAT-Code/dto/
# make install
# reboot
~~~

2. run input-events
~~~
# input-events 0
~~~

3. press any key on display board
