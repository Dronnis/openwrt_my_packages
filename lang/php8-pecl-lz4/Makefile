include $(TOPDIR)/rules.mk

PECL_NAME:=lz4
PECL_LONGNAME:=PHP extension for interfacing with lz4

PKG_VERSION:=0.0.1
PKG_RELEASE:=1

PKG_NAME:=php8-pecl-lz4
PKG_SOURCE_URL:=https://github.com/kjdev/php-ext-lz4.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=2f006c3e4f1fb3a60d2656fc164f9ba26b71e995
PKG_MIRROR_HASH:=ccd43eb40a6e6b355fd2220340fa5688b248c63d1d3d8b95f447e1a2c38a7afc
PKG_SOURCE_DATE:=2022-12-12

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=README.md

PKG_BUILD_DEPENDS:=php8 liblz4
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-lz4-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-lz4-includedir="$(STAGING_DIR)/usr" 

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+liblz4,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
