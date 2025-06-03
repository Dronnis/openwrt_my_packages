include $(TOPDIR)/rules.mk

PECL_NAME:=igbinary
PECL_LONGNAME:=PHP extension for interfacing with Igbinary

PKG_VERSION:=3.2.16
PKG_RELEASE:=2
PKG_HASH:=8bf25d465abc7973d9e2c9a3039a5f8eea635b23bc1477017ff3999ff95836da

PKG_NAME:=php8-pecl-igbinary
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
	--enable-igbinary 

define Build/InstallDev
	mkdir -p $(STAGING_DIR)/usr/include/php8/ext/igbinary/src/php7/$(PECL_NAME)/
	$(CP) $(PKG_BUILD_DIR)/src/php7/*.h $(STAGING_DIR)/usr/include/php8/ext/igbinary/src/php7/
	$(CP) $(PKG_BUILD_DIR)/{php_igbinary,igbinary}.h $(STAGING_DIR)/usr/include/php8/ext/igbinary
endef


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
