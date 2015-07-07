# auto generated makefile
HPT_ROOT := /usr/src/rr232x-linux-src-v1.10.patch2
HPT_REGPARM := $(shell echo "$(CFLAGS) $(KBUILD_CFLAGS)" | awk '{ match($$0,"-mregparm="); if (RSTART>0) print substr($$0,RSTART+10,1);}')
HPT_REGPARM := $(if $(HPT_REGPARM),$(HPT_REGPARM),0)
HPT_LIB := /usr/src/rr232x-linux-src-v1.10.patch2/lib/linux/free-x86_64-regparm$(HPT_REGPARM)
TARGETNAME := rr232x
TARGETOBJS := os_linux.o osm_linux.o div64.o hptinfo.o config.o
TARGETMODS := him_rr232x.o ldm_raid50.o partition.o raid0.o raid1.o raid5.o jbod.o

obj-m := $(TARGETNAME).o

$(TARGETNAME)-objs := $(TARGETOBJS) $(TARGETMODS)

EXTRA_CFLAGS := -DLINUX -D_LINUX_ -D__KERNEL__=1 -DSUPPORT_ARRAY -DDBG=0 -DBITS_PER_LONG=64 -DMODVERSIONS -DMODULE -Idrivers/scsi -I$(HPT_ROOT)/inc/linux -I$(HPT_ROOT)/inc -I$(HPT_ROOT)/osm/linux

$(addprefix $(obj)/,$(TARGETOBJS:.o=.c)): FORCE
	@{ test -f /usr/src/rr232x-linux-src-v1.10.patch2/product/rr232x/linux/$(notdir $@) && cp -f /usr/src/rr232x-linux-src-v1.10.patch2/product/rr232x/linux/$(notdir $@) $@; } ||\
	{ test -f $(HPT_ROOT)/osm/linux/$(notdir $@) && cp -f $(HPT_ROOT)/osm/linux/$(notdir $@) $@; }

$(addprefix $(obj)/,$(TARGETMODS)): $(obj)/%.o: $(HPT_LIB)/%.o
	@cp -f $< $@
