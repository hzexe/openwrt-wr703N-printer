#
# Copyright (C) 2012-2016 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/host.mk

ARCH:=arm
BOARD:=brcm2708
BOARDNAME:=Broadcom BCM27xx
FEATURES:=ext4 audio usb usbgadget display gpio fpu
MAINTAINER:=Álvaro Fernández Rojas <noltari@gmail.com>
SUBTARGETS:=bcm2708 bcm2709 bcm2710

KERNEL_PATCHVER:=4.4

define Target/Description
	Build firmware image for Broadcom BCM27xx SoC devices.
	Currently produces SD Card image for Raspberry Pi.
endef

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += brcm2708-gpu-fw kmod-usb-hid kmod-sound-core kmod-sound-arm-bcm2835 kmod-fs-vfat kmod-nls-cp437 kmod-nls-iso8859-1

KERNELNAME:=Image dtbs

$(eval $(call BuildTarget))
