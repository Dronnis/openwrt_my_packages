

include $(TOPDIR)/rules.mk



PECL_NAME:=xxhash
PECL_LONGNAME:=This extension is a PHP binding for the xxhash library.

PKG_VERSION:=0.2.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/pmmp/ext-xxhash.git
PKG_SOURCE_VERSION:=e565182a5234ab4c757dd81762fa8647ad20ee58
PKG_MIRROR_HASH:=02bc49a5acffe8774ef36f5d91819c48d2c14e2086005def9ab3212d0b3d84ad


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=None
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-xxhash


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
