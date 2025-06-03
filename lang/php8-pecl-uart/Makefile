include $(TOPDIR)/rules.mk




PECL_NAME:=uart
PECL_LONGNAME:=The UART PHP Extension provides an object-oriented wrapper to the UART Linux Kernel driver that gives users the ability to write code that interacts with external hardware using the UART asynchronous serial communication protocol.
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/embedded-php/ext-uart.git
PKG_SOURCE_VERSION:=59a2aff23574cebf2d50361e4c6a700e8e706af0
PKG_MIRROR_HASH:=skip


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-uart

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
