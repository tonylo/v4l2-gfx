#
# This makefile is used when building for l24 (Linux) as part of the
# SGX kernel services DDK
#
# To add to the DDK (whose top level dir is EURASIAROOT, edit the file:
# $(EURASIAROOT)/eurasiacon/build/linux/omap4430_linux/kbuild
#
# Add an entry refering to the location containing this directory:
#	EXTRA_SUBDIRS += $(EURASIAROOT)/services4/v4l2-gfx/ddk
#

MODULE		= gfx_vout_mod

V4L2GFXIOCTLHEADERPATH=$(EURASIAROOT)/services4/v4l2-gfx/include

INCLUDES = \
		-I$(EURASIAROOT)/include4 \
		-I$(EURASIAROOT)/services4/include \
		-I$(V4L2GFXIOCTLHEADERPATH)

SOURCES =	../../gfx_init.c \
			../../gfx_io.c \
			../../gfx_bc.c \
			../../gfx_tiler.c

SYM_VERS_DEPS = $(EURASIAROOT)/services4/srvkm/env/linux

include $(EURASIAROOT)/eurasiacon/build/linux/kbuild/Makefile.kbuild_subdir_common
