#
# This program is free software; you can redistribute it and/or modify it under
# the terms of the GNU General Public License as published by the Free Software
# Foundation; either version 2 of the License, or (at your option) any later
# version.  This program is distributed in the hope that it will be useful, but
# without any warranty; without even the implied warranty of mechantability or
# fitness for a particular purpose.  See the GNU General Public License for
# more details.  You should have received a copy of the GNU General Public
# License along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
#
# Nathan L. Conrad <nathan@noreply.alt-teknik.com>
#
# adapted for can-obd. Seel A. alexanderseel86@googlemail.com 

ifneq ($(KERNELRELEASE),)
	ccflags-y += -I$(PROJECT_DIR)/include/uapi
	obj-m := can-obd.o
	can-obd-objs := obd.o
else
	KERNELDIR ?= /lib/modules/$(shell uname -r)/build
modules:
	$(MAKE) -C $(KERNELDIR) M=$(shell pwd) modules
modules_install:
	$(MAKE) -C $(KERNELDIR) M=$(shell pwd) modules_install
endif
