include $(TOPDIR)/rules.mk

PECL_NAME:=mailparse
PECL_LONGNAME:=PHP extension for interfacing with mailparse

PKG_VERSION:=3.1.8
PKG_RELEASE:=2
PKG_HASH:=59beab4ef851770c495ba7a0726ab40e098135469a11d9c8e665b089c96efc2f

PKG_NAME:=php8-pecl-mailparse
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-mailparse


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
