
################################################################################
#
# Common Variables that already set:
#     LICHEE_KDIR
#     LICHEE_MOD_DIR
#     CROSS_COMPILE
#     ARCH
#
#################################################################################
PWD=$(shell pwd)
obj-m+=nand.o 
nand-objs := nand_interface.o  \
             nfd/nand_blk.o nfd/nand_osal_for_linux.o libnand_sun8iw6p1.a

install: build
	cp nand.ko $(LICHEE_MOD_DIR)/

build:
	@echo $(LICHEE_KDIR)
	cp libnand_sun8iw6p1 libnand_sun8iw6p1.a
	$(MAKE) -C $(LICHEE_KDIR) M=$(PWD)


clean:
	@rm -rf *.o *.ko .*.cmd *.mod.c *.order *.symvers .tmp_versions *~
