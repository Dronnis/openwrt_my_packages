include $(TOPDIR)/rules.mk

PECL_NAME:=simdjson
PECL_LONGNAME:=Provides faster json decoding through simdjson bindings for PHP

PKG_VERSION:=4.0.0
PKG_RELEASE:=1
PKG_HASH:=1fb48fe579ff0b6b8f991f236c0caed1645f672baa2abf7b3f8c9f21488119c8

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=Apache 2.0
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-simdjson


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
