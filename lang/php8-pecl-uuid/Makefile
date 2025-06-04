include $(TOPDIR)/rules.mk

PECL_NAME:=uuid
PECL_LONGNAME:=PHP extension for interfacing with uuid

PKG_VERSION:=1.2.1
PKG_RELEASE:=1
PKG_HASH:=2235c8584ca8911ce5512ebf791e5bb1d849c323640ad3e0be507b00156481c7

PKG_NAME:=php8-pecl-uuid
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=LGPL
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 uuid
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-uuid="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libuuid))
$(eval $(call BuildPackage,$(PKG_NAME)))