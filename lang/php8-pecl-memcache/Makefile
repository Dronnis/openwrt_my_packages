include $(TOPDIR)/rules.mk

PECL_NAME:=memcache
PECL_LONGNAME:=PHP extension memcached

PKG_VERSION:=8.2
PKG_RELEASE:=2
PKG_HASH:=b3f0640eacdeb9046c6c86a1546d7fb8a4e9f219e5d9a36a287e59b2dd8208e5

PKG_NAME:=php8-pecl-memcache
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 zlib
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-memcache\
	--with-zlib-dir="$(STAGING_DIR)/usr" 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+zlib))
$(eval $(call BuildPackage,$(PKG_NAME)))
