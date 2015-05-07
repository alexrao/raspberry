obj-m :=hello.o
KERNELDIR :=/mnt/workspace/raspberry/tools/rpi_linux_kernel
PWD :=$(shell pwd)
all:
	make -C $(KERNELDIR) M=$(PWD) modules
	
.PHONY :clean
clean:
	rm -rf *.o *ko Module.symvers *.mod.c  modules.order .tmp_versions .*.ko.cmd  .*.o.cmd 
