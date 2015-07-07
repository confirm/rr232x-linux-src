# $Id: Makefile,v 1.3 2006/01/20 10:39:56 gmm Exp $
#
# Copyright (C) 2005 HighPoint Technologies, Inc.
# All Rights Reserved.
#

HPT_ROOT := ../../..

C_DEFINES := -DSUPPORT_ARRAY

TARGETNAME := rr232x
TARGETTYPE := KMOD
TARGETMODS := him_rr232x.o ldm_raid50.o partition.o raid0.o raid1.o raid5.o jbod.o
TARGETOBJS := os_linux.o osm_linux.o div64.o hptinfo.o config.o

include $(HPT_ROOT)/inc/linux/Makefile.def

$(TARGETOBJS): osm_linux.h
