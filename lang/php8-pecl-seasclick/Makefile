include $(TOPDIR)/rules.mk

PECL_NAME:=SeasClick
PECL_LONGNAME:=PHP extension for An Yandex ClickHouse client driven extension for PHP.

PKG_VERSION:=0.1.1
PKG_RELEASE:=1
PKG_HASH:=d08818ffe8cd7d530e5c71eb5be273dc89ae79a4ce3603240d0685a5587100b3

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP 3.01
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	 --enable-SeasClick


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
