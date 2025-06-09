include $(TOPDIR)/rules.mk

PECL_NAME:=maxminddb
PECL_LONGNAME:=PHP extension for interfacing with maxminddb

PKG_VERSION:=1.12.1
PKG_RELEASE:=1
PKG_HASH:=12e0db583e961700725b14c880d529bc93cac0db22ab7bd0fde8a926e478bfb5

PKG_NAME:=php8-pecl-maxminddb
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=Apache License 2.0
PKG_LICENSE_FILES:=COPYING
PKG_BUILD_DEPENDS:=php8 libmaxminddb
#PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	 --with-maxminddb 

define Build/Prepare
	$(Build/Prepare/Default)
	cp -fR $(PKG_BUILD_DIR)/../maxminddb-$(PKG_VERSION)/ext/* $(PKG_BUILD_DIR)
	$(if $(QUILT),,( cd $(PKG_BUILD_DIR); $(STAGING_DIR)/usr/bin/phpize8 ))
endef
$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libmaxminddb))
$(eval $(call BuildPackage,$(PKG_NAME)))
