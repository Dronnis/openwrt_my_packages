include $(TOPDIR)/rules.mk

PECL_NAME:=oauth
PECL_LONGNAME:=PHP extension for  oauth consumer extension

PKG_VERSION:=2.0.9
PKG_RELEASE:=1
PKG_HASH:=05fe20322256db62e7bcb5a45693ebc59829eae264f855d5b1438003ab34efe1

PKG_NAME:=php8-pecl-$(PECL_NAME)
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
	--enable-oauth


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
