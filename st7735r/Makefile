obj-m += st7735r.o

KERNELDIR ?= /lib/modules/$(shell uname -r)

all:
	make -C $(KERNELDIR)/build M=$(PWD) modules

clean:
	make -C $(KERNELDIR)/build M=$(PWD) clean

install:
	xz -c st7735r.ko > $(KERNELDIR)/kernel/drivers/gpu/drm/tiny/st7735r.ko.xz