include $(TOPDIR)/rules.mk

PECL_NAME:=spx
PECL_LONGNAME:=PHP extension simple profiler for PHP

PKG_VERSION:=0.4.18
PKG_RELEASE:=1

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/NoiseByNorthwest/php-spx.git
PKG_SOURCE_VERSION:=6a5f0ce44b285d9c566a38fae3a25ed0eb26058e
PKG_MIRROR_HASH:=c4fc70d26103b61a680df41657315cc6823e0f05544a75a45fcf5c273eec7d7e

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 zlib
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-spx \
	--with-zlib-dir="$(STAGING_DIR)/usr"

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+zlib))
$(eval $(call BuildPackage,$(PKG_NAME)))
