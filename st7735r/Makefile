obj-m += st7735r.o

KERNELDIR ?= /lib/modules/$(shell uname -r)
SOURCE ?= https://github.com/raspberrypi/linux/raw/HEAD/drivers/gpu/drm/tiny/st7735r.c

all: st7735r.ko

clean:
	make -C $(KERNELDIR)/build M=$(PWD) clean

install:
	xz -c st7735r.ko > $(KERNELDIR)/kernel/drivers/gpu/drm/tiny/st7735r.ko.xz

st7735r.ko: st7735r.c
	make -C $(KERNELDIR)/build M=$(PWD) modules

st7735r.c: st7735r.c.origin
	git apply calibration-offset.patch

st7735r.c.origin:
	wget -O st7735r.c.origin $(SOURCE)
