include $(TOPDIR)/rules.mk

PECL_NAME:=msgpack
PECL_LONGNAME:=PHP extension for interfacing with msgpack

PKG_VERSION:=3.0.0
PKG_RELEASE:=2
PKG_HASH:=55306a84797d399c6b269181ec484634f18bea1330bbd9d7405043c597de69cd

PKG_NAME:=php8-pecl-msgpack
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
	--with-msgpack

define Build/InstallDev
	mkdir -p $(STAGING_DIR)/usr/include/php8/ext/msgpack
	$(CP) $(PKG_BUILD_DIR)/php_msgpack.h $(STAGING_DIR)/usr/include/php8/ext/msgpack
endef

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),))
$(eval $(call BuildPackage,$(PKG_NAME)))
