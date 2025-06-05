include $(TOPDIR)/rules.mk

PECL_NAME:=snappy
PECL_LONGNAME:=PHP extension for this extension allows Snappy.

PKG_VERSION:=0.2.3
PKG_RELEASE:=1
PKG_HASH:=skip

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/kjdev/php-ext-snappy.git
PKG_SOURCE_VERSION:=c65734c9374c3cc2d0101cc06424555e2880a0ee
PKG_MIRROR_HASH:=13239d3882fed2beb298985a78a4d88fd30c972e3eaf6f21b96d8b2215baa39f

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License 3.01
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libsnappy
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-snappy 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libsnappy))
$(eval $(call BuildPackage,$(PKG_NAME)))
