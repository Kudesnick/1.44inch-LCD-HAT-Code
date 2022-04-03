# 1.44inch-LCD-HAT

Original instruction: https://www.waveshare.com/wiki/1.44inch_LCD_HAT
Original code: https://www.waveshare.com/w/upload/f/fa/1.44inch-LCD-HAT-Code.7z

Tested on Raspberry Pi Zero W.

1. Enable SPI interface:
~~~
sudo sed -i "s/#dtparam=spi=on/dtparam=spi=on/" "/boot/config.txt"
sudo reboot
~~~

2. Install python packages:
~~~
sudo apt install python3-numpy
sudo pip install python3-pil
~~~

3. Download code:
~~~
git clone https://github.com/kudesnick/1.44inch-LCD-HAT-Code.git
~~~

4. Run test:
~~~
cd 1.44inch-LCD-HAT-Code/RaspberryPi/python/
python main.py
~~~

