ifeq ($(DEBUG),y)
  DEBFLAGS = -O -g -DSCULLC_DEBUG # "-O" is needed to expand inlines
else
  DEBFLAGS = -O2
endif

EXTRA_CFLAGS  += $(DEBFLAGS) -I$(LDDINC)
TARGET = led
scullc-objs :=  led_gpio.o
obj-m :=led.o 
KERNELDIR :=/mnt/workspace/raspberry/tools/rpi_linux_kernel
PWD :=$(shell pwd)
all:
	make -C $(KERNELDIR) M=$(PWD)  LDDINC=$(PWD)  modules

install:
	install -d $(INSTALLDIR)
	install -c $(TARGET).o $(INSTALLDIR)	

.PHONY :clean
clean:
	rm -rf *.o *ko Module.symvers *.mod.c  modules.order .tmp_versions .*.ko.cmd  .*.o.cmd 
