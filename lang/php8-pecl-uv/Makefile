include $(TOPDIR)/rules.mk

PECL_NAME:=uv
PECL_LONGNAME:=PHP extension for interfacing with uv

PKG_VERSION:=0.3.0
PKG_RELEASE:=2
PKG_HASH:=a11f9c987f4c466b70c79050714fcf0c916753c560421279bbe0f6b7dc737d3e

PKG_NAME:=php8-pecl-uv
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libuv
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-uv="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libuv))
$(eval $(call BuildPackage,$(PKG_NAME)))
