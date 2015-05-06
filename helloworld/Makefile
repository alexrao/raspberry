obj-m :=hello.o
KERNELDIR :=/mnt/workspace/raspberry/tools/rpi_linux_kernel
PWD :=$(shell pwd)
all:
	make -C $(KERNELDIR) M=$(PWD) modules
	
.PHONY :clean
clean:
	rm -rf *.o *ko
