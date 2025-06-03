#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk




PECL_NAME:=i2c
PECL_LONGNAME:=PHP Extension I2C provides an object-oriented wrapper to the i2c-dev Linux Module that gives users the ability to write code that interacts with external hardware using the I2C protocol.

PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/embedded-php/ext-i2c.git
PKG_SOURCE_VERSION:=185327d847a92c77a9f6b8a074a532d4260070c5
PKG_MIRROR_HASH:=skip


#PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tar.zst


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 i2c-tools
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=patch-libtool

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-i2c

#define Build/InstallDev
	#mkdir -p $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)
	#cp $(PKG_BUILD_DIR)/php_phalcon.h $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)/
#endef

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +i2c-tools,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
