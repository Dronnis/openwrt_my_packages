#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk




PECL_NAME:=gpio
PECL_LONGNAME:=PHP Extension GPIO  provides an object-oriented wrapper to the gpio Linux Userspace ABI that gives users the ability to write code that interacts with the general-purpose input/output pins available in Linux-based

PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/embedded-php/ext-gpio.git
PKG_SOURCE_VERSION:=57a2caa738832fcac8405f84cbd084039cf6efc6
PKG_MIRROR_HASH:=skip


#PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tar.zst


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
	--with-gpio

#define Build/InstallDev
	#mkdir -p $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)
	#cp $(PKG_BUILD_DIR)/php_phalcon.h $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)/
#endef

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
